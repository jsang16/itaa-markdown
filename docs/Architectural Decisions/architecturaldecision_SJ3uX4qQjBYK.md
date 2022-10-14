

# OCP-001

### Name

Hosting Platform and Managed or Self-Managed Service

### Status

accepted

### Last Update

2022-03-08

### Subject Area

OCP-Platform

### Topic



### Issue or Problem Statement

Select which hosting platform should RHOCP cluster be installed on, and what kind of managed service is required (managed or self-managed). While often this is a business decision or a customer requirement, IBM should guide the customer in selecting the right platform and management level. When selecting self-managed options (such as IPI or UPI), you can also position / design managed services from IBM Consulting or 3rd party providers. Consider that more than one platform can be used, in a multi-cloud design.

### Assumptions

Reference: https://cloud.redhat.com/products

### Motivation

OpenShift is available as a managed cloud service (from Azure, AWS or IBM Cloud), as a managed service from Red Hat (OpenShift Dedicated) or can be deployed as a self-managed platform through IPI or UPI installations.

### Notes



[Expand all](#){ .md-button .same-line }

### Alternatives


    

<details markdown=1>
<summary markdown="span">Cloud Service: Microsoft Azure Red Hat OpenShift (ARO) </summary>

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
        <td>Cloud Service: Microsoft Azure Red Hat OpenShift (ARO) </td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Billed by: Microsoft, managed by Red Hat and Microsoft, Supported by: Red Hat and Microsoft</td>
    </tr>
    <tr>
        <td> <strong>Best Applied</strong> </td>
        <td>When the client indicated a strong preference for Azure and has associated workloads.</td>
    </tr>
    <tr>
        <td> <strong>Contraindications</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Cloud Service: Red Hat OpenShift Dedicated, Cloud hosted: AWS or GCP, Billed by Red Hat and cloud provider, managed by: Red Hat, supported by Red Hat</summary>

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
        <td>Cloud Service: Red Hat OpenShift Dedicated, Cloud hosted: AWS or GCP, Billed by Red Hat and cloud provider, managed by: Red Hat, supported by Red Hat</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Cloud Service: Red Hat OpenShift Dedicated, Cloud hosted: AWS or GCP, Billed by Red Hat and cloud provider, managed by: Red Hat, supported by Red Hat</td>
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
<summary markdown="span">Cloud Service: Red Hat OpenShift Service on AWS (ROSA), hosted on AWS, Billed by: AWS, Managed by: Red Hat and AWS, Supported by: Red Hat and AWS</summary>

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
        <td>Cloud Service: Red Hat OpenShift Service on AWS (ROSA), hosted on AWS, Billed by: AWS, Managed by: Red Hat and AWS, Supported by: Red Hat and AWS</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Cloud Service: Red Hat OpenShift Service on AWS (ROSA), hosted on AWS, Billed by: AWS, Managed by: Red Hat and AWS, Supported by: Red Hat and AWS</td>
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
<summary markdown="span">Cloud Service: Red Hat OpenShift on IBM Cloud Satellite</summary>

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
        <td>Cloud Service: Red Hat OpenShift on IBM Cloud Satellite</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Managed by: IBM Cloud, Billed By: IBM Cloud or Bring Your Own License (BYOL), Supported by: IBM and Red Hat</td>
    </tr>
    <tr>
        <td> <strong>Best Applied</strong> </td>
        <td>On-prem, AWS, Azure or other hyperscalers when IBM Cloud is the lead provider for multi-cloud environment</td>
    </tr>
    <tr>
        <td> <strong>Contraindications</strong> </td>
        <td>When the client refuses to use IBM Cloud</td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Cloud Service: Red Hat OpenShift on IBM Cloud, hosted on IBM Cloud, billed by IBM, Managed by: IBM, supported by: Red Hat and IBM</summary>

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
        <td>Cloud Service: Red Hat OpenShift on IBM Cloud, hosted on IBM Cloud, billed by IBM, Managed by: IBM, supported by: Red Hat and IBM</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Cloud Service: Red Hat OpenShift on IBM Cloud, hosted on IBM Cloud, billed by IBM, Managed by: IBM, supported by: Red Hat and IBM</td>
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
<summary markdown="span">Cloud Service: Red hat OpenShift on IBM VMware, hosted on IBM IC4RW. self managed by Client or IBM</summary>

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
        <td>Cloud Service: Red hat OpenShift on IBM VMware, hosted on IBM IC4RW. self managed by Client or IBM</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Cloud Service: Red hat OpenShift on IBM VMware, hosted on IBM IC4RW. self managed by Client or IBM</td>
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
<summary markdown="span">Self Managed (on Bare Metal or Virtual Nodes, see decision 2)</summary>

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
        <td>Self Managed (on Bare Metal or Virtual Nodes, see decision 2)</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>See Architecture AD-002 for platform type and installation type.</td>
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



