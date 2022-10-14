

# OCP-003

### Name

OpenShift Self Managed - IPI or UPI installation

### Status

accepted

### Last Update

2022-03-08

### Subject Area

OCP-Platform

### Topic



### Issue or Problem Statement

Deploy OpenShift as a IPI or UPI installation. When designing an IPI or UPI deployment, consider if additional 'managed services' are provided to the customer (ex: NordCloud, IBM Consulting Platform Engineering Services, etc). and ensure they are supported across the platform design.

### Assumptions

Choosing IPI over UPI will provide additional capabilities for OpenShift to auto-scale and manage infrastructure elements. IPI installation is not supported across all platforms, please check the documentation for the specific OpenShift version you plan to deploy. Ex:  <a href="https://docs.openshift.com/container-platform/4.9/installing/installing-preparing.html" target="_blank">https://docs.openshift.com/container-platform/4.9/installing/installing-preparing.html</a><div><br></div>

### Motivation

<a href="https://docs.openshift.com/container-platform/4.9/installing/installing-preparing.html" target="_blank">https://docs.openshift.com/container-platform/4.9/installing/installing-preparing.html</a>

### Notes



[Expand all](#){ .md-button .same-line }

### Alternatives


    

<details markdown=1>
<summary markdown="span">IPI - Installer Provisioned Infrastructure</summary>

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
        <td>IPI - Installer Provisioned Infrastructure</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>IPI</td>
    </tr>
    <tr>
        <td> <strong>Best Applied</strong> </td>
        <td>When IPI installation is supported</td>
    </tr>
    <tr>
        <td> <strong>Contraindications</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">UPI - User Provisioned Infrastructure</summary>

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
        <td>UPI - User Provisioned Infrastructure</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>UPI</td>
    </tr>
    <tr>
        <td> <strong>Best Applied</strong> </td>
        <td>When IPI is not supported, or requires certain customizations.</td>
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



