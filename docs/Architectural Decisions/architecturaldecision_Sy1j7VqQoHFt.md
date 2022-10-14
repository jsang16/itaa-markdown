

# OCP-008

### Name

Management Service Placement

### Status

accepted

### Last Update

2022-03-08

### Subject Area

OCP-Platform

### Topic

Infrastructure Nodes

### Issue or Problem Statement

Configure dedicated infrastructure nodes for OpenShift cluster

### Assumptions

Infrastructure nodes: Instances (virtual or physical hosts) of Red Hat Enterprise Linux or Red Hat Enterprise Linux CoreOS that are running pods supporting Red Hat OpenShift’s cluster infrastructure or running the HAProxy-based load balancer for ingress traffic. Infrastructure nodes are included in self-managed Red Hat OpenShift subscriptions.

### Motivation

<div><a href="https://www.redhat.com/en/technologies/cloud-computing/openshift/subscription-guide" target="_blank">https://www.redhat.com/en/technologies/cloud-computing/openshift/subscription-guide</a></div><div><br></div><div><b>OpenShift Control Plane and Infrastructure nodes</b><br><br>Each self-managed Red Hat OpenShift subscription provides extra entitlements for Red Hat OpenShift, Red Hat Enterprise Linux, and other Red Hat OpenShift-related components. These extra entitlements are included for the purpose of running Red Hat OpenShift control plane and infrastructure nodes.<br>Infrastructure nodes<br><br>The Red Hat OpenShift installer deploys a highly available Red Hat OpenShift control plane composed of 3 control plane nodes, in addition to Red Hat OpenShift worker nodes to run end user applications. <br><br>By default, Kubernetes control plane components (e.g., API server, etcd, scheduler) and supporting cluster services (e.g., monitoring, registry) will be deployed on the Red Hat OpenShift control plane nodes. However, customers may decide to move some of these supporting cluster services to dedicated infrastructure nodes.<br><br>To qualify as an infrastructure node and use the included entitlement, only components that are supporting the cluster, and not part of an end user application, may be running on those instances.<br><br>Examples include:<br><br>    Red Hat OpenShift registry<br>    Red Hat OpenShift Ingress Router (local and global/multicluster ingress)<br>    Red Hat OpenShift monitoring<br>    Red Hat OpenShift log management<br>    HAProxy-based instances used for cluster ingress<br>    Red Hat Quay<br>    Red Hat OpenShift Data Foundation (previously Red Hat OpenShift Container Storage)<br>    Red Hat Advanced Cluster Management for Kubernetes<br>    Red Hat Advanced Cluster Security for Kubernetes<br>    Red Hat OpenShift GitOps<br>    Red Hat OpenShift Pipelines<br><br>Customers may deploy and run custom and third-party agents and tools for monitoring, log data collection and forwarding, hardware drivers, infrastructure integration such as virtualization agents, etc. to infrastructure nodes without disqualifying the node for infrastructure licensing.<br><br>However, this is limited only to agents and related components, including controller Pods for Operators. It does not include the custom or third-party software suite. Examples of these may include:<br><br>    Custom and third-party monitoring agents<br>    Container network interface (CNI) and container storage interface (CSI) drivers and controllers (plugins)<br>    Hardware or virtualization enablement accelerators<br>    Controller pods used for Kubernetes CRD or Operators (custom or third-party software)<br><br>No other end user application instances or types may be run on an infrastructure node using the included entitlement. To run other infrastructure workloads as application instances on Red Hat OpenShift, you must run those instances on regular application nodes. Verify infrastructure status qualifications with Red Hat.<br>Additional approved usage of the infrastructure node<br><br>As end users increase their usage of Red Hat OpenShift, they may begin using some of the more sophisticated application deployment patterns. As a result, they may need to add additional software components to the platform.<br><br>As a general principle, Red Hat OpenShift subscriptions are based on the total capacity of the Red Hat OpenShift worker nodes that are required to run the application workloads and supporting application services deployed to those worker nodes. <br></div>

### Notes



[Expand all](#){ .md-button .same-line }

### Alternatives


    

<details markdown=1>
<summary markdown="span">Isolate management function (Add Infrastructure Nodes)</summary>

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
        <td>Isolate management function (Add Infrastructure Nodes)</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Isolating management functions in dedicated nodes is highly recommended.
Red Hat OpenShift has multiple infrastructure components[^11.1]:

Default router
Container image registry
Cluster metrics collection, or monitoring service
Cluster aggregated logging
Service brokers
It is recommended to separate the infrastructure nodes for monitoring and logging.
Collocating infrastructure functions may be feasible when performance is not a requirement such as in Dev/Test environments.</td>
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


    

<details markdown=1>
<summary markdown="span">Management function on control plane node</summary>

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
        <td>Management function on control plane node</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Kubernetes management functions such as monitoring, and logging are memory intensive workloads with a lot of Disk IO.
Size a smaller management node when cost is an issue.</td>
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



