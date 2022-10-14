

# OCP-011

### Name

Control Plane Deployment Topology (Single Region with multiple AZ)

### Status

proposed

### Last Update

2022-03-08

### Subject Area

Platform

### Topic



### Issue or Problem Statement

Deployment topology for OpenShift clusters across one or more Regions, with one or more availability zones.

### Assumptions

The workloads should support running across multiple clusters in different regions. OpenShift does not support stretched clusters across multiple regions as the latency requirements for replicating etcd require deploying the control plane across one or more Availability Zones within the same geographic region.

### Motivation

There are different reasons to have multiple regions , which include: 
- High availability for highly distributed applications
- Disaster Recovery set up
- Multiple Geo-presence, allowing workloads to be closer to their end consumers 
- Regulatory compliance. For example data residency requirements; processes that need to run in certain jurisdictions; etc

### Notes



[Expand all](#){ .md-button .same-line }

### Alternatives


    

<details markdown=1>
<summary markdown="span">Single Region Deployment</summary>

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
        <td>Single Region Deployment</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>OpenShift will be deployed between 1 or more AZ within a region.</td>
    </tr>
    <tr>
        <td> <strong>Best Applied</strong> </td>
        <td>If a workload does not support running across multiple regions and high latency, then a multi availability zone in a single region may be a better option. 
If high availability requirements include running a workload in multiple DCs, this could be accomplished by using Availability Zones with some Public Cloud providers. You need to check the specific Availability Zone set up for the  Hyperscalers where you're looking to install OpenShift.</td>
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



