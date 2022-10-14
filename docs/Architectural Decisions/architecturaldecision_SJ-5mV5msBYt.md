

# OCP-010

### Name

Application Availability

### Status

accepted

### Last Update

2022-03-08

### Subject Area

OCP-Workload

### Topic



### Issue or Problem Statement

Resilient application deployment patterns across multiple regions, zones, nodes.

### Assumptions

Data replication / persistent storage is resolved in some form, and we're looking at ways to ensure the applications themselves remain highly available in case of partial outage (zone, region, node, etc).

### Motivation

Application deployment patterns for meeting certain SLAs, SLOs, RTO, RPO, etc.<div><br></div>

### Notes



[Expand all](#){ .md-button .same-line }

### Alternatives


    

<details markdown=1>
<summary markdown="span">Multi-zone cluster</summary>

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
        <td>Multi-zone cluster</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Cloud providers, as well as many clients, have multiple data centers which provide low-latency, multi-zone capabilities.
Multi-zone clusters across 3 availability zones support both High-Availability and Disaster Recovery[^7.1].</td>
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
<summary markdown="span">Multiple clusters across zones or regions</summary>

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
        <td>Multiple clusters across zones or regions</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Stretched clusters across multiple regions using underlying technology (ex: VMWare) to move control plane nodes across regions is not recommended.
For the most critical workloads, load-balancing multiple clusters across different availability zones and/or regions can provide continuous application availability, this will ensure the following:

Increases the resiliency against potential zone failures.
Protects application from zone failures in environments where multi-zone capabilities are not available.</td>
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
<summary markdown="span">Single zone cluster</summary>

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
        <td>Single zone cluster</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Application availability selection will vary based on solution requirements and Service Level Objectives.
Single zone clusters provide protection against node failures, but not against zone failure including networks and storage.</td>
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



