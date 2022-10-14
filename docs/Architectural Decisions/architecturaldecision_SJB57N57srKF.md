

# OCP-017

### Name

Load Balancer Selection

### Status

proposed

### Last Update

2022-03-08

### Subject Area

Platform

### Topic



### Issue or Problem Statement

Identify the appropriate Load Balancer / Ingress when using OpenShift across various platforms.

### Assumptions

https://docs.openshift.com/container-platform/4.9/networking/configuring_ingress_cluster_traffic/overview-traffic.html

### Motivation



### Notes



[Expand all](#){ .md-button .same-line }

### Alternatives


    

<details markdown=1>
<summary markdown="span">Combination of both</summary>

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
        <td>Combination of both</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Configuration of the router and load-balancer policies is required with either option.
Specialized knowledge of vendor load-balancer product is required.
GTM (Global Traffic Managers)/LTM (Local Traffic Managers) provide load-balancing and traffic routing capabilities based on the service availability across multiple zones/DCs and/or regions.</td>
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
<summary markdown="span">External load-balancer</summary>

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
        <td>External load-balancer</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>External load-balancers require additional cost.</td>
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
<summary markdown="span">Red Hat OpenShift routes</summary>

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
        <td>Red Hat OpenShift routes</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Red Hat OpenShift provides a built-in routes service, which provides load-balancing capabilities at no additional cost; however, without external load-balancer it relies on DNS load-balancing which has its own limitations.</td>
    </tr>
    <tr>
        <td> <strong>Best Applied</strong> </td>
        <td>Default option for most cases.</td>
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



