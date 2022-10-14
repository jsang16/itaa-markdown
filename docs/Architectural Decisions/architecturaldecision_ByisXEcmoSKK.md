

# OCP-018

### Name

Storage Technology for Red Hat OpenShift Cluster Platform Registry

### Status

proposed

### Last Update

2022-03-08

### Subject Area

Storage

### Topic

Storage type

### Issue or Problem Statement



### Assumptions

For Bare Metal deployment:<div>https://docs.openshift.com/container-platform/4.6/registry/configuring_registry_storage/configuring-registry-storage-baremetal.html#installation-registry-storage-config_configuring-registry-storage-baremetal</div>

### Motivation

OpenShift Container Platform supports ReadWriteOnce access for image registry storage when you have only one replica. To deploy an image registry that supports high availability with two or more replicas, ReadWriteMany access is required.<br><div><br></div><div>https://docs.openshift.com/container-platform/4.9/registry/configuring_registry_storage/configuring-registry-storage-vsphere.html#installation-registry-storage-config_configuring-registry-storage-vsphere</div><div><br></div><div>Testing shows issues with using the NFS server on RHEL as storage backend for core services. This includes the OpenShift Container Registry and Quay, Prometheus for monitoring storage, and Elasticsearch for logging storage. Therefore, using RHEL NFS to back PVs used by core services is not recommended.</div><div><br></div><div>Other NFS implementations on the marketplace might not have these issues. Contact the individual NFS implementation vendor for more information on any testing that was possibly completed against these OpenShift Container Platform core components.</div>

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
        <td>File storage and block storage are not recommended for a scaled/HA Red Hat OpenShift Container Platform registry cluster deployment with production workloads.</td>
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
        <td>File storage and block storage are not recommended for a scaled/HA Red Hat OpenShift Container Platform registry cluster deployment with production workloads.</td>
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
        <td>The preferred storage technology is object storage for both scaled and non-scaled Red Hat OpenShift Registry.</td>
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



