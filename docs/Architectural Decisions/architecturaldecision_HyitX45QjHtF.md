

# OCP-009

### Name

Production and Non-Production Topology

### Status

accepted

### Last Update

2022-03-08

### Subject Area

OCP-Platform

### Topic



### Issue or Problem Statement

OpenShift Projects (namespaces) provide a certain degree of isolation between different development teams or environments, but don't provide full isolation from denial of services, resource consumption and require proper management to provide even basic resource constraint isolation.

### Assumptions



### Motivation

Customers may request that production environments are separated from non-production environments.

### Notes



[Expand all](#){ .md-button .same-line }

### Alternatives


    

<details markdown=1>
<summary markdown="span">Multi-Tenant clusters for non-production workloads</summary>

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
        <td>Multi-Tenant clusters for non-production workloads</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Large Multi-Tenant Clusters based on nodes isolation can be used to provide more strict segmentation within the cluster.
Multi-Tenant Cluster with Namespace isolation may be used for small workloads that are too small to justify the cost of a single-tenant cluster that is highly available across multiple zones[^5.1].
It is generally recommended to merge the dev and test in one non-production cluster separating them through Red Hat OpenShift Projects (namespaces).</td>
    </tr>
    <tr>
        <td> <strong>Best Applied</strong> </td>
        <td>Customer need tenant isolation to meet certain isolation requirement. such as regulator compliance, which means that it cannot be hosted across other tenants or clients. 
When you want to reduce costs by merging non-production environments, but still separate production.</td>
    </tr>
    <tr>
        <td> <strong>Contraindications</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Single-Tenant clusters</summary>

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
        <td>Single-Tenant clusters</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Single-tenant cluster can be used to separate Dev, Test &amp; Prod Environments with varying requirements.
Single-tenant clusters provide pod privileges without putting other tenants at risk of being compromised and enable teams with complex services to have control over the lifecycle of the cluster.</td>
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



