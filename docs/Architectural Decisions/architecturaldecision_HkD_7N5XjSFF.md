

# OCP-002

### Name

Red Hat OpenShift Cluster Platform Node Type

### Status

accepted

### Last Update

2022-03-08

### Subject Area

OCP-Platform

### Topic



### Issue or Problem Statement

When allocating infrastructure resources for Cluster nodes, what compute infrastructure should be chosen?

### Assumptions

In general, decision for using bare metal or virtualized nodes for RHOCP is supported across all platforms.

### Motivation

Please refer to the latest matrix of supported IPI / UPI and node types here: <a href="https://docs.openshift.com/container-platform/4.9/installing/installing-preparing.html" target="_blank">https://docs.openshift.com/container-platform/4.9/installing/installing-preparing.html</a>

### Notes



[Expand all](#){ .md-button .same-line }

### Alternatives


    

<details markdown=1>
<summary markdown="span">Bare-Metal</summary>

<table>
    <caption></caption>
    <thead>
        <tr>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tr>
        <td> <strong>Name</strong> </td>
        <td>Bare-Metal</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Bare-metal is most suited to Data, Memory, or Compute intensive workloads as well as those requiring high-performance and/or GPU-intensive workloads.
Bare-metal removes the overhead of hypervisor licenses, but introduces management complexity and reduced flexibility.
Use of Bare-metal for control plane nodes would result in inefficient use of resources.
See link in motivation with regard to supported installation on different bare metal architectures (x86, Power, Z)</td>
    </tr>
    <tr>
        <td> <strong>Best Applied</strong> </td>
        <td>Using Bare Metal will allow you to support OpenShift Virtualization: https://docs.openshift.com/container-platform/4.9/virt/about-virt.html
Bare metal is selected to meet compute and GPU intensive workloads as hosting on VM or hypervisor could deprive or not fulfill the requirements</td>
    </tr>
    <tr>
        <td> <strong>Contraindications</strong> </td>
        <td>Circumstances where the client wants to scale in and out in small increments.</td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Hybrid (x86 ONLY)</summary>

<table>
    <caption></caption>
    <thead>
        <tr>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tr>
        <td> <strong>Name</strong> </td>
        <td>Hybrid (x86 ONLY)</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Hybrid cluster with mixed node types is also a possibility. The common approach for this hybrid cluster is to have control plane nodes as virtual while having the worker nodes as Bare-metal. The rationale is that client data-centers would most probably don't have small enough physical machines to host the control plane nodes so it's possible to have the control plane nodes on virtual for optimization purposes. While having a BareMetal worker nodes as large as the workload requires.</td>
    </tr>
    <tr>
        <td> <strong>Best Applied</strong> </td>
        <td>when using IBM Cloud (Classic) with Bare Metal worker nodes: using the same architecture (x86) you need to mix Bare Metal and Virtual node types, to support different workload types.</td>
    </tr>
    <tr>
        <td> <strong>Contraindications</strong> </td>
        <td>Mixed node type complicates Day 2 operations management.
Need to keep nodes on a common machine host architecture within a single cluster management</td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Virtual Dedicated</summary>

<table>
    <caption></caption>
    <thead>
        <tr>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tr>
        <td> <strong>Name</strong> </td>
        <td>Virtual Dedicated</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Virtual Dedicated runs on dedicated hardware and is fast to deploy and scale.
It provides the necessary security and performance to support production workloads.

Virtual Dedicated is best suited for clients that requests fully dedicated hardware.</td>
    </tr>
    <tr>
        <td> <strong>Best Applied</strong> </td>
        <td>No noisy neighbors
Compliance requirements</td>
    </tr>
    <tr>
        <td> <strong>Contraindications</strong> </td>
        <td>More expensive than virtual shared on all hypervisors</td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Virtual Shared</summary>

<table>
    <caption></caption>
    <thead>
        <tr>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tr>
        <td> <strong>Name</strong> </td>
        <td>Virtual Shared</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Shared Virtual is cheap and fast to deploy, but not suitable for business critical or performance workloads.</td>
    </tr>
    <tr>
        <td> <strong>Best Applied</strong> </td>
        <td>The simplest and standard option.  Use this option unless there is a requirement that pushes to another alternative.</td>
    </tr>
    <tr>
        <td> <strong>Contraindications</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    



### Decision



### Justification



### Implications

https://www.redhat.com/en/technologies/cloud-computing/openshift/subscription-guide#openshift-container-platform
1. Type of supported installation (IPI or UPI deployment) - https://docs.openshift.com/container-platform/4.9/installing/installing-preparing.html
2. Optimal licensing (per CPU core / vCPU pair or per socket subscriptions) - https://www.redhat.com/en/technologies/cloud-computing/openshift/subscription-guide#openshift-container-platform

### Derived Requirements



### Related Decisions



