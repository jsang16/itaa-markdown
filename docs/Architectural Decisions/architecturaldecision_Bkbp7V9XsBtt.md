

# OCP-016

### Name

Ingress Traffic for Applications

### Status

accepted

### Last Update

2022-03-08

### Subject Area

OCP-Workload

### Topic



### Issue or Problem Statement

OpenShift Container Platform provides the different methods for communicating from outside the cluster with services running in the cluster.

### Assumptions

This decision depends on many factors such as application traffic, type of the traffic (http or https or mix), and TLS termination point (do the routers terminate TLS or they do pass-through for the https).

### Motivation

<a href="https://docs.openshift.com/container-platform/4.9/networking/configuring_ingress_cluster_traffic/overview-traffic.html" target="_blank">https://docs.openshift.com/container-platform/4.9/networking/configuring_ingress_cluster_traffic/overview-traffic.html</a>

### Notes



[Expand all](#){ .md-button .same-line }

### Alternatives


    

<details markdown=1>
<summary markdown="span">Dedicated routers on dedicated nodes</summary>

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
        <td>Dedicated routers on dedicated nodes</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Depending on the applications requirements a dedicated Red Hat OpenShift routers may be needed to handle the applications traffic.
A minimum of two routers should be considered for each application group that requires dedicated routers for the ingress traffic.
Depending on the traffic more than two routers may need to be deployed.
The dedicated routers may share the workers with the applications or may be deployed on the dedicated ones.</td>
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
<summary markdown="span">Dedicated routers sharing nodes with applications</summary>

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
        <td>Dedicated routers sharing nodes with applications</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Depending on the applications requirements a dedicated Red Hat OpenShift routers may be needed to handle the applications traffic.
A minimum of two routers should be considered for each application group that requires dedicated routers for the ingress traffic.
Depending on the traffic more than two routers may need to be deployed.
The dedicated routers may share the workers with the applications or may be deployed on the dedicated ones.</td>
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
<summary markdown="span">Default shared routers</summary>

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
        <td>Default shared routers</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>By default all ingress traffic is sharing the default routers.</td>
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



