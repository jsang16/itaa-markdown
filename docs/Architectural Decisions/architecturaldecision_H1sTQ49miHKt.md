

# OCP-006

### Name

Control plane node sizing

### Status

accepted

### Last Update

2022-03-08

### Subject Area

OCP-Platform

### Topic

Sizing

### Issue or Problem Statement

•Control plane node sizes cannot be changed in a running cluster for OpenShift version 4.7 or lower<div>As of version 4.8, a rolling upgrade is supported (shut down one of the masters, modify by adding CPU or memory and restart) - <a href="https://access.redhat.com/solutions/5597381" target="_blank">https://access.redhat.com/solutions/5597381</a><br><div><div><div><div>• For 4.7 or lower, the total worker node count must be estimated in advance as this determines recommended control plane node size during installation.
•Control plane node sizing should balance scalability and cost</div></div></div></div></div>

### Assumptions

The alternatives below assume a typical virtualized environment running on x86. For other architectures (Z, POWER) or bare metal servers with higher end CPUs, adjust accordingly.

### Motivation

<div>Scaling the OpenShift control plane to match the cluster size dynamically </div><div><a href="https://www.ibm.com/cloud/architecture/articles/ibmaot-redhat-openshift/02-solutions-guide-capacity-planning-capacity-planning" target="_blank">https://www.ibm.com/cloud/architecture/articles/ibmaot-redhat-openshift/02-solutions-guide-capacity-planning-capacity-planning</a></div>

### Notes



[Expand all](#){ .md-button .same-line }

### Alternatives


    

<details markdown=1>
<summary markdown="span">Large – 16vCPU x 64GB RAM</summary>

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
        <td>Large – 16vCPU x 64GB RAM</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Large – 16vCPU x 64GB RAM</td>
    </tr>
    <tr>
        <td> <strong>Best Applied</strong> </td>
        <td>This is recommended in cases where cluster needs to support more than 100 worker nodes.</td>
    </tr>
    <tr>
        <td> <strong>Contraindications</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Medium – 8vCPU x 32GB RAM</summary>

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
        <td>Medium – 8vCPU x 32GB RAM</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Medium – 8vCPU x 32GB RAM</td>
    </tr>
    <tr>
        <td> <strong>Best Applied</strong> </td>
        <td>This is a common production cluster sizing and supports 0-100 worker nodes.</td>
    </tr>
    <tr>
        <td> <strong>Contraindications</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Small – 4vCPU x 16GB RAM</summary>

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
        <td>Small – 4vCPU x 16GB RAM</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Small – 4vCPU x 16GB RAM</td>
    </tr>
    <tr>
        <td> <strong>Best Applied</strong> </td>
        <td></td>
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



### Derived Requirements



### Related Decisions



