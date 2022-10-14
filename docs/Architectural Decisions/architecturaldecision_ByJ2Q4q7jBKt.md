

# OCP-019

### Name

Storage Technology for Metrics & Logging

### Status

proposed

### Last Update

2021-11-11

### Subject Area

Storage

### Topic

Storage for metrics and logging

### Issue or Problem Statement

A persistent volume is required for each Elasticsearch deployment configuration. On OpenShift Container Platform this is achieved using persistent volume claims.<div><br></div><div>Using NFS storage as a volume or a persistent volume (or via NAS such as Gluster) is not supported for Elasticsearch storage, as Lucene relies on file system behavior that NFS does not supply. Data corruption and other problems can occur.</div>

### Assumptions

The OpenShift Elasticsearch Operator names the PVCs using the Elasticsearch resource name.<div><br></div><div>Fluentd ships any logs from systemd journal and /var/log/containers/ to Elasticsearch.</div><div><br></div><div>Elasticsearch requires sufficient memory to perform large merge operations. If it does not have enough memory, it becomes unresponsive. To avoid this problem, evaluate how much application log data you need, and allocate approximately double that amount of free storage capacity.</div><div><br></div><div>By default, when storage capacity is 85% full, Elasticsearch stops allocating new data to the node. At 90%, Elasticsearch attempts to relocate existing shards from that node to other nodes if possible. But if no nodes have a free capacity below 85%, Elasticsearch effectively rejects creating new indices and becomes RED.</div>

### Motivation

https://docs.openshift.com/container-platform/4.9/logging/config/cluster-logging-storage-considerations.html<div>https://docs.openshift.com/container-platform/4.9/logging/config/cluster-logging-log-store.html#cluster-logging-elasticsearch-storage_cluster-logging-store</div>

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
        <td>The preferred storage technology for Metrics &amp; Logging is Block Storage.</td>
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
        <td>For small deployments local disk may be sufficient.</td>
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



