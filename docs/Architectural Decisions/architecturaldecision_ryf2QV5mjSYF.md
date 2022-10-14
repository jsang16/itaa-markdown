

# OCP-020

### Name

Persistent Storage Options for Applications

### Status

proposed

### Last Update

2022-03-08

### Subject Area

Storage

### Topic

Workload storage

### Issue or Problem Statement

Select the storage providers available to OpenShift, that match the application workloads and required replication / availability of the data. Note that various Cloud Paks support different storage providers, and different Cloud Providers / platforms have varying support for these storage providers. For this AD, please check against the latest Cloud Pak / workload documentation, as well as the platform documentation (ex: AWS) to ensure you have a supported combination.

### Assumptions

Storage requirements vary from application to application.
Development teams should select best storage option for their application.
For the best etcd reliability, the lowest consistent latency storage technology is preferable.
Documented Red Hat OpenShift Reference Architectures provides several potential options based on defined solution requirements.

### Motivation

https://docs.openshift.com/container-platform/4.9/storage/understanding-persistent-storage.html<div>https://ibm.seismic.com/Link/Content/DCMgg8H37dqfG8qPhMFg3XWH2BdG for more details on supported storage drivers for IBM Cloud Paks</div><div>https://ibm.seismic.com/Link/Content/DCPWVTpXb4m228mMQ9QR2MPf72MV for hyperscaler options</div><div>https://pages.github.ibm.com/UDF/UDF-Guide/t/T101385/ - other details on storage ADs</div>

### Notes



[Expand all](#){ .md-button .same-line }

### Alternatives


    

<details markdown=1>
<summary markdown="span">Block Storage</summary>

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
        <td>Block Storage</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Block storage does not support concurrent access.
Databases tend to perform best with dedicated, block storage</td>
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
<summary markdown="span">File Storage (NAS)</summary>

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
        <td>File Storage (NAS)</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>N/A</td>
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
<summary markdown="span">Local Volumes</summary>

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
        <td>Local Volumes</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Red Hat OpenShift PVs can be provisioned using local volumes[^18.2].
Local volumes are subject to the availability of the underlying node and are not suitable for all applications.</td>
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
<summary markdown="span">NetApp Trident</summary>

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
        <td>NetApp Trident</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>N/A</td>
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
<summary markdown="span">Object Storage</summary>

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
        <td>Object Storage</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Object storage is not consumed through Red Hat OpenShift PVs/ PVCs.
Object storage must have drivers built into the application and/or container.</td>
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
<summary markdown="span">Portworx</summary>

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
        <td>Portworx</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>For IBM Cloud Paks, you need to check which storage solution is supported for each IBM Cloud Pak. For example the disaster recovery of IBM Cloud Pak for Data depends on Portworx Asynchronous replication.
Some IBM Cloud Paks gives limited entitlements for some storage solutions. For example, IBM Cloud Pak for Integration gives entitlement to Storage Suite for IBM Cloud Paks (to be used for up to 12 TB of Red Hat OpenShift Data Foundation and an additional capacity of 12 TB across the rest of the storage offerings) while IBM Cloud Pak for Data gives entitlement for Portworx Essential (up to 128 VPC or 8 worker nodes whatever is lower). However, IBM doesn't recommend to use Portworx Essential on Production. Refer to the license document information for the specific terms and conditions related to these entitlements.</td>
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
<summary markdown="span">Red Hat OpenShift Data Foundation</summary>

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
        <td>Red Hat OpenShift Data Foundation</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Red Hat OpenShift Data Foundation is available as a persistent storage options as of Red Hat OpenShift V4.3[^18.3].
Red Hat OpenShift Data Foundation is completely integrated with Red Hat OpenShift Container Platform for deployment, management, and monitoring.</td>
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
<summary markdown="span">vSphere Volumes</summary>

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
        <td>vSphere Volumes</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>vSphere Volumes provide RWO access-modes. So it cannot be used in case the application requires RWX.</td>
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



