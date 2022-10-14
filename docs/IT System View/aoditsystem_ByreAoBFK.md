
## Diagram

![04 Cloud cluster](../img/aoditsystem_ByreAoBFK.png)



### Name


04 Cloud cluster


### Description


Requirement: Higher availability solution.<div><br></div><div><ul><li>Deploy cluster over availability zones (AZ).</li></ul></div><div>Number of AZ: 3</div><div><br></div><div>This topology has been tested and validated on public cloud: Amazon Web Services (AWS), Microsoft® Azure®, Google Cloud Platform, and IBM Cloud®.</div><div><br></div><div>Nodes are spread over the 3 AZ.</div><div><br></div><div>Number of nodes:</div><div><ul><li>3 master1 nodes</li><li>3 worker nodes</li><li>3 infrastructure nodes</li></ul></div><div>Note: The number of nodes and their sizing can be adjusted depending on the workload target. See the capacity sizing chapter.</div><div><br></div><div>Typical use cases:</div><div><br></div><div><ul><li>Development</li><li>Test</li><li>Integration</li><li>Production with limited SLA</li></ul></div>


## Element

[Expand all](#){ .md-button .diff-line }


### Actor


    

<details markdown=1>
<summary markdown="span">Cloud Storage</summary>

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
        <td>Cloud Storage</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Storage for persistent volumes is provided by an external tier solution.
Not embedded into the Red Hat OpenShift Container Platform cluster. It could be, but not limited to:
    NFS server (not recommended for production)
    VMware® Vsphere® Volumes

https://www.ibm.com/cloud/architecture/articles/ibmaot-redhat-openshift/02-solutions-guide-solution-design-reference-architecture</td>
    </tr>
    <tr>
        <td> <strong>Type</strong> </td>
        <td>IT System</td>
    </tr>
    <tr>
        <td> <strong>Generic Group</strong> </td>
<td>
        
</td>
    </tr>
</table>


</details>


    




### Subsystem


    

<details markdown=1>
<summary markdown="span">Compute Plane</summary>

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
        <td>Compute Plane</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>A physical server that acts as a hypervisor and contains the processing capabilities required to run virtual machines in the environment. A basic RHOSP environment requires at least one Compute node.<br><br><div><a href="https://access.redhat.com/documentation/en-us/red_hat_openstack_platform/16.0/html/director_installation_and_usage/planning-your-overcloud " target="_blank">https://access.redhat.com/documentation/en-us/red_hat_openstack_platform/16.0/html/director_installation_and_usage/planning-your-overcloud </a></div><div><br></div></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Control Plane</summary>

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
        <td>Control Plane</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>The control plane, which is composed of master machines, manages the OpenShift Container Platform cluster. <div><br></div><div><a href="https://docs.openshift.com/container-platform/4.1/architecture/control-plane.html " target="_blank">https://docs.openshift.com/container-platform/4.1/architecture/control-plane.html </a></div><div><br></div></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Infrastructure Plane</summary>

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
        <td>Infrastructure Plane</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>You can use infrastructure machine sets to create machines that host only infrastructure components, such as the default router, the integrated container image registry, and the components for cluster metrics and monitoring. These infrastructure machines are not counted toward the total number of subscriptions that are required to run the environment.<br><br><div><a href="https://docs.openshift.com/container-platform/4.7/machine_management/creating-infrastructure-machinesets.html " target="_blank">https://docs.openshift.com/container-platform/4.7/machine_management/creating-infrastructure-machinesets.html </a></div><div><br></div></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Red Hat OpenShift Container Platform</summary>

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
        <td>Red Hat OpenShift Container Platform</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Red Hat® OpenShift® offers a consistent hybrid cloud foundation for building and scaling containerized applications. Benefit from streamlined platform installation and upgrades from one of the enterprise Kubernetes leaders.<br><br><div><a href="https://cloud.redhat.com/products/container-platform" target="_blank">https://cloud.redhat.com/products/container-platform</a></div><div><br></div></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Storage Plane</summary>

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
        <td>Storage Plane</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>It provides file, block, and object storage classes, enabling a wide range of data modalities and workloads, including:<br>Data at rest, such as databases and data warehouses.<br>Data in motion, automating data pipelines.<br>Data in action, providing services for continuous deployment models, analytics, artificial intelligence (AI), and machine learning (ML).<br><a href="https://www.redhat.com/en/resources/openshift-data-foundation-datasheet" target="_blank">https://www.redhat.com/en/resources/openshift-data-foundation-datasheet</a><div><br></div></td>
    </tr>
</table>


</details>


    




### Location


    

<details markdown=1>
<summary markdown="span">AZ1</summary>

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
        <td>AZ1</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>The requirement is a high-available solution.<div>Deploy cluster over availability zones (AZ).</div><div>Storage solution is managed by Cloud provider across AZ.</div><div>This topology has been tested and validated on public cloud, such as Amazon Web Services (AWS), Microsoft® Azure®, Google Cloud Platform (GCP), and IBM Cloud®.</div><div>Candidate storage solutions: IBM Cloud Storage, Amazon Elastic Block Store, Azure Files</div><div><a href="https://www.ibm.com/cloud/architecture/articles/ibmaot-redhat-openshift/02-solutions-guide-solution-design-reference-architecture " target="_blank">https://www.ibm.com/cloud/architecture/articles/ibmaot-redhat-openshift/02-solutions-guide-solution-design-reference-architecture </a></div><div><br></div></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">AZ2</summary>

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
        <td>AZ2</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>The requirement is a high-available solution.<div>Deploy cluster over availability zones (AZ).</div><div>Storage solution is managed by Cloud provider across AZ.</div><div>This topology has been tested and validated on public cloud, such as Amazon Web Services (AWS), Microsoft® Azure®, Google Cloud Platform (GCP), and IBM Cloud®.</div><div>Candidate storage solutions: IBM Cloud Storage, Amazon Elastic Block Store, Azure Files</div><div><a href="https://www.ibm.com/cloud/architecture/articles/ibmaot-redhat-openshift/02-solutions-guide-solution-design-reference-architecture " target="_blank">https://www.ibm.com/cloud/architecture/articles/ibmaot-redhat-openshift/02-solutions-guide-solution-design-reference-architecture </a></div><div><br></div></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">AZ3</summary>

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
        <td>AZ3</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>The requirement is a high-available solution.<div>Deploy cluster over availability zones (AZ).</div><div>Storage solution is managed by Cloud provider across AZ.</div><div>This topology has been tested and validated on public cloud, such as Amazon Web Services (AWS), Microsoft® Azure®, Google Cloud Platform (GCP), and IBM Cloud®.</div><div>Candidate storage solutions: IBM Cloud Storage, Amazon Elastic Block Store, Azure Files</div><div><a href="https://www.ibm.com/cloud/architecture/articles/ibmaot-redhat-openshift/02-solutions-guide-solution-design-reference-architecture " target="_blank">https://www.ibm.com/cloud/architecture/articles/ibmaot-redhat-openshift/02-solutions-guide-solution-design-reference-architecture </a></div><div><br></div></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Location</summary>

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
        <td>Location</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Region</summary>

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
        <td>Region</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    




### Logical Connection


    

<details markdown=1>
<summary markdown="span"></summary>

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
        <td></td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span"></summary>

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
        <td></td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span"></summary>

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
        <td></td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span"></summary>

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
        <td></td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span"></summary>

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
        <td></td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span"></summary>

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
        <td></td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span"></summary>

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
        <td></td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span"></summary>

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
        <td></td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span"></summary>

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
        <td></td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span"></summary>

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
        <td></td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span"></summary>

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
        <td></td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span"></summary>

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
        <td></td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span"></summary>

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
        <td></td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span"></summary>

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
        <td></td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span"></summary>

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
        <td></td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span"></summary>

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
        <td></td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td></td>
    </tr>
</table>


</details>


    



### Logical Node


    

<details markdown=1>
<summary markdown="span">Compute node 1</summary>

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
        <td>Compute node 1</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Compute nodes are responsible for running virtual machine instances after they are launched. Compute nodes require bare metal systems that support hardware virtualization. Compute nodes must also have enough memory and disk space to support the requirements of the virtual machine instances that they host.

https://access.redhat.com/documentation/en-us/red_hat_openstack_platform/10/html/director_installation_and_usage/chap-requirements</td>
    </tr>
    <tr>
        <td> <strong>Type</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Primary Capability</strong> </td>
        <td>
            
                <div>container image</div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Implementation</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Architectural Decision</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Non Functional Requirement</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Generic Group</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Sub-level Diagram</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Related Diagrams</strong> </td>
        <td>
            
                <div><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></div>
            
                <div><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></div>
            
                <div><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></div>
            
                <div><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Related Elements</strong> </td>
        <td>
            
            
                <div>container image</div>
                
            
        </td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Compute node 2</summary>

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
        <td>Compute node 2</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Compute nodes are responsible for running virtual machine instances after they are launched. Compute nodes require bare metal systems that support hardware virtualization. Compute nodes must also have enough memory and disk space to support the requirements of the virtual machine instances that they host.


https://access.redhat.com/documentation/en-us/red_hat_openstack_platform/10/html/director_installation_and_usage/chap-requirements</td>
    </tr>
    <tr>
        <td> <strong>Type</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Primary Capability</strong> </td>
        <td>
            
                <div>container image</div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Implementation</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Architectural Decision</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Non Functional Requirement</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Generic Group</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Sub-level Diagram</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Related Diagrams</strong> </td>
        <td>
            
                <div><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></div>
            
                <div><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></div>
            
                <div><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></div>
            
                <div><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Related Elements</strong> </td>
        <td>
            
            
                <div>container image</div>
                
            
        </td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Compute node 3</summary>

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
        <td>Compute node 3</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Compute nodes are responsible for running virtual machine instances after they are launched. Compute nodes require bare metal systems that support hardware virtualization. Compute nodes must also have enough memory and disk space to support the requirements of the virtual machine instances that they host.

https://access.redhat.com/documentation/en-us/red_hat_openstack_platform/10/html/director_installation_and_usage/chap-requirements</td>
    </tr>
    <tr>
        <td> <strong>Type</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Primary Capability</strong> </td>
        <td>
            
                <div>container image</div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Implementation</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Architectural Decision</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Non Functional Requirement</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Generic Group</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Sub-level Diagram</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Related Diagrams</strong> </td>
        <td>
            
                <div><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></div>
            
                <div><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></div>
            
                <div><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></div>
            
                <div><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Related Elements</strong> </td>
        <td>
            
            
                <div>container image</div>
                
            
        </td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Compute plane load balancer</summary>

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
        <td>Compute plane load balancer</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Use a load balancer service to distribute traffic among your application servers residing locally within data center.<div><br></div><div><a href="https://cloud.ibm.com/catalog/infrastructure/load-balancer-group" target="_blank">https://cloud.ibm.com/catalog/infrastructure/load-balancer-group</a></div></td>
    </tr>
    <tr>
        <td> <strong>Type</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Primary Capability</strong> </td>
        <td>
            
                <div>network routing</div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Implementation</strong> </td>
        <td>
            
                <div><a href="https://www.ibm.com/cloud/load-balancer"> IBM Cloud Load Balancers</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Architectural Decision</strong> </td>
        <td>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_SJB57N57srKF">Load Balancer Selection</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Non Functional Requirement</strong> </td>
        <td>
            
                <div><a href="../../Non Functional Requirements/nonfunctionalrequirement_H1es1ZgIFK">Load balancing</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Generic Group</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Sub-level Diagram</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Related Diagrams</strong> </td>
        <td>
            
                <div><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></div>
            
                <div><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Related Elements</strong> </td>
        <td>
            
                <div>Load balancing</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></li>
                    
                
            
                <div>Load Balancer Selection</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_By7NIorFt">02 Three nodes cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></li>
                    
                
            
            
                <div>SYS_DU_38v3qxufxWL</div>
                
            
                <div>network routing</div>
                
            
        </td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Control plane load balancer</summary>

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
        <td>Control plane load balancer</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Use a load balancer service to distribute traffic among your application servers residing locally within data center.

https://cloud.ibm.com/catalog/infrastructure/load-balancer-group</td>
    </tr>
    <tr>
        <td> <strong>Type</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Primary Capability</strong> </td>
        <td>
            
                <div>network routing</div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Implementation</strong> </td>
        <td>
            
                <div><a href="https://www.ibm.com/cloud/load-balancer"> IBM Cloud Load Balancers</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Architectural Decision</strong> </td>
        <td>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_SJB57N57srKF">Load Balancer Selection</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Non Functional Requirement</strong> </td>
        <td>
            
                <div><a href="../../Non Functional Requirements/nonfunctionalrequirement_H1es1ZgIFK">Load balancing</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Generic Group</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Sub-level Diagram</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Related Diagrams</strong> </td>
        <td>
            
                <div><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></div>
            
                <div><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></div>
            
                <div><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Related Elements</strong> </td>
        <td>
            
                <div>Load balancing</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></li>
                    
                
            
                <div>Load Balancer Selection</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_By7NIorFt">02 Three nodes cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></li>
                    
                
            
            
                <div>SYS_DU_37sFycoSa3m</div>
                
            
                <div>network routing</div>
                
            
        </td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Control Plane node 1</summary>

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
        <td>Control Plane node 1</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>In a Kubernetes cluster, the control plane nodes run services that are required to control the Kubernetes cluster. They contain more than just the Kubernetes services for managing the OpenShift Container Platform cluster. Instead of being grouped into a MachineSet, control plane machines are defined by a series of standalone machine API resources. Extra controls apply to control plane machines to prevent you from deleting all control plane machines and breaking your cluster.


https://docs.openshift.com/container-platform/4.9/architecture/control-plane.html</td>
    </tr>
    <tr>
        <td> <strong>Type</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Primary Capability</strong> </td>
        <td>
            
                <div>container platform</div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Implementation</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Architectural Decision</strong> </td>
        <td>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_H1sTQ49miHKt">Control plane node sizing</a></div>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_Hk0F7VcXjrYY">Control Plane Deployment Topology</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Non Functional Requirement</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Generic Group</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Sub-level Diagram</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Related Diagrams</strong> </td>
        <td>
            
                <div><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></div>
            
                <div><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></div>
            
                <div><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></div>
            
                <div><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Related Elements</strong> </td>
        <td>
            
                <div>Control plane node sizing</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></li>
                    
                
            
                <div>Control Plane Deployment Topology</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></li>
                    
                
            
            
                <div>container platform</div>
                
            
        </td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Control Plane node 2</summary>

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
        <td>Control Plane node 2</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>In a Kubernetes cluster, the control plane nodes run services that are required to control the Kubernetes cluster. They contain more than just the Kubernetes services for managing the OpenShift Container Platform cluster. Instead of being grouped into a MachineSet, control plane machines are defined by a series of standalone machine API resources. Extra controls apply to control plane machines to prevent you from deleting all control plane machines and breaking your cluster.<br><br><br>https://docs.openshift.com/container-platform/4.9/architecture/control-plane.html</td>
    </tr>
    <tr>
        <td> <strong>Type</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Primary Capability</strong> </td>
        <td>
            
                <div>container platform</div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Implementation</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Architectural Decision</strong> </td>
        <td>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_Hk0F7VcXjrYY">Control Plane Deployment Topology</a></div>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_SJ3uX4qQjBYK">Hosting Platform and Managed or Self-Managed Service</a></div>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_H1sTQ49miHKt">Control plane node sizing</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Non Functional Requirement</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Generic Group</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Sub-level Diagram</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Related Diagrams</strong> </td>
        <td>
            
                <div><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></div>
            
                <div><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></div>
            
                <div><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></div>
            
                <div><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Related Elements</strong> </td>
        <td>
            
                <div>Control Plane Deployment Topology</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></li>
                    
                
            
                <div>Hosting Platform and Managed or Self-Managed Service</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></li>
                    
                
            
                <div>Control plane node sizing</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></li>
                    
                
            
            
                <div>container platform</div>
                
            
        </td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Control Plane node 3</summary>

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
        <td>Control Plane node 3</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>In a Kubernetes cluster, the control plane nodes run services that are required to control the Kubernetes cluster. They contain more than just the Kubernetes services for managing the OpenShift Container Platform cluster. Instead of being grouped into a MachineSet, control plane machines are defined by a series of standalone machine API resources. Extra controls apply to control plane machines to prevent you from deleting all control plane machines and breaking your cluster.<br><br><br>https://docs.openshift.com/container-platform/4.9/architecture/control-plane.html</td>
    </tr>
    <tr>
        <td> <strong>Type</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Primary Capability</strong> </td>
        <td>
            
                <div>application runtime</div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Implementation</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Architectural Decision</strong> </td>
        <td>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_Hk0F7VcXjrYY">Control Plane Deployment Topology</a></div>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_SJ3uX4qQjBYK">Hosting Platform and Managed or Self-Managed Service</a></div>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_H1sTQ49miHKt">Control plane node sizing</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Non Functional Requirement</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Generic Group</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Sub-level Diagram</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Related Diagrams</strong> </td>
        <td>
            
                <div><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></div>
            
                <div><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></div>
            
                <div><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></div>
            
                <div><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Related Elements</strong> </td>
        <td>
            
                <div>Control Plane Deployment Topology</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></li>
                    
                
            
                <div>Hosting Platform and Managed or Self-Managed Service</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></li>
                    
                
            
                <div>Control plane node sizing</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_r18uxVqXsBFK">01 Starter environment</a></li>
                    
                
            
            
        </td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Infra node 1</summary>

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
        <td>Infra node 1</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>It is recommended to separate the infrastructure nodes for monitoring, logging, metrics, registry, and router components. Therefore, the recommendation is to dedicate three infrastructure nodes for these functionalities. See this link from Red Hat Documentation for more details about Creating Infrastructure Machine Set.

Separating these functionalities in a dedicated infrastructure machine set will free up more space in your worker nodes for your workload to run.

Additionally, these infrastructure nodes don't consume from the customer's Red Hat OpenShift subscription, which is why you should consider having them separated.

Collocating management functions may be feasible when performance is not required, such as in Dev/Test environments, to save the infrastructure-related costs.


https://www.ibm.com/cloud/architecture/articles/ibmaot-redhat-openshift/02-solutions-guide-solution-design-solution-architecture</td>
    </tr>
    <tr>
        <td> <strong>Type</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Primary Capability</strong> </td>
        <td>
            
                <div>container platform</div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Implementation</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Architectural Decision</strong> </td>
        <td>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_Sy1j7VqQoHFt">Management Service Placement</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Non Functional Requirement</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Generic Group</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Sub-level Diagram</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Related Diagrams</strong> </td>
        <td>
            
                <div><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></div>
            
                <div><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></div>
            
                <div><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></div>
            
                <div><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Related Elements</strong> </td>
        <td>
            
                <div>Management Service Placement</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                
            
            
                <div>container platform</div>
                
            
        </td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Infra node 2</summary>

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
        <td>Infra node 2</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>It is recommended to separate the infrastructure nodes for monitoring, logging, metrics, registry, and router components. Therefore, the recommendation is to dedicate three infrastructure nodes for these functionalities. See this link from Red Hat Documentation for more details about Creating Infrastructure Machine Set.

Separating these functionalities in a dedicated infrastructure machine set will free up more space in your worker nodes for your workload to run.

Additionally, these infrastructure nodes don't consume from the customer's Red Hat OpenShift subscription, which is why you should consider having them separated.

Collocating management functions may be feasible when performance is not required, such as in Dev/Test environments, to save the infrastructure-related costs.


https://www.ibm.com/cloud/architecture/articles/ibmaot-redhat-openshift/02-solutions-guide-solution-design-solution-architecture</td>
    </tr>
    <tr>
        <td> <strong>Type</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Primary Capability</strong> </td>
        <td>
            
                <div>container platform</div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Implementation</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Architectural Decision</strong> </td>
        <td>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_Sy1j7VqQoHFt">Management Service Placement</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Non Functional Requirement</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Generic Group</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Sub-level Diagram</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Related Diagrams</strong> </td>
        <td>
            
                <div><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></div>
            
                <div><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></div>
            
                <div><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></div>
            
                <div><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Related Elements</strong> </td>
        <td>
            
                <div>Management Service Placement</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                
            
            
                <div>container platform</div>
                
            
        </td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Infra node 3</summary>

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
        <td>Infra node 3</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>It is recommended to separate the infrastructure nodes for monitoring, logging, metrics, registry, and router components. Therefore, the recommendation is to dedicate three infrastructure nodes for these functionalities. See this link from Red Hat Documentation for more details about Creating Infrastructure Machine Set.

Separating these functionalities in a dedicated infrastructure machine set will free up more space in your worker nodes for your workload to run.

Additionally, these infrastructure nodes don't consume from the customer's Red Hat OpenShift subscription, which is why you should consider having them separated.

Collocating management functions may be feasible when performance is not required, such as in Dev/Test environments, to save the infrastructure-related costs.


https://www.ibm.com/cloud/architecture/articles/ibmaot-redhat-openshift/02-solutions-guide-solution-design-solution-architecture</td>
    </tr>
    <tr>
        <td> <strong>Type</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Primary Capability</strong> </td>
        <td>
            
                <div>container platform</div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Implementation</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Architectural Decision</strong> </td>
        <td>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_Sy1j7VqQoHFt">Management Service Placement</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Non Functional Requirement</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Generic Group</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Sub-level Diagram</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Related Diagrams</strong> </td>
        <td>
            
                <div><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></div>
            
                <div><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></div>
            
                <div><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></div>
            
                <div><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Related Elements</strong> </td>
        <td>
            
                <div>Management Service Placement</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                
            
            
                <div>container platform</div>
                
            
        </td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Storage node 1</summary>

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
        <td>Storage node 1</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Storage for persistent volumes is embedded into the cluster and managed as containers. Some examples are:

Rook Ceph
Red Hat OpenShift Data Foundation   
Portworx

Dedication of storage nodes. Isolate storage workload on specific nodes. There are pods, deployed on the cluster that are managing access to storage resource. Alternative: storage nodes could be merged with compute nodes (min 3 worker nodes) but it could have impacts on performance.</td>
    </tr>
    <tr>
        <td> <strong>Type</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Primary Capability</strong> </td>
        <td>
            
                <div>container platform</div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Implementation</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Architectural Decision</strong> </td>
        <td>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_ByJ2Q4q7jBKt">Storage Technology for Metrics & Logging</a></div>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_ByisXEcmoSKK">Storage Technology for Red Hat OpenShift Cluster Platform Registry</a></div>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_ryf2QV5mjSYF">Persistent Storage Options for Applications</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Non Functional Requirement</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Generic Group</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Sub-level Diagram</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Related Diagrams</strong> </td>
        <td>
            
                <div><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></div>
            
                <div><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></div>
            
                <div><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></div>
            
                <div><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Related Elements</strong> </td>
        <td>
            
                <div>Storage Technology for Metrics & Logging</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                
            
                <div>Storage Technology for Red Hat OpenShift Cluster Platform Registry</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                
            
                <div>Persistent Storage Options for Applications</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                
            
            
                <div>container platform</div>
                
            
        </td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Storage node 2</summary>

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
        <td>Storage node 2</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Storage for persistent volumes is embedded into the cluster and managed as containers. Some examples are:

 Rook Ceph
 Red Hat OpenShift Data Foundation   
 Portworx
Dedication of storage nodes. Isolate storage workload on specific nodes. There are pods, deployed on the cluster that are managing access to storage resource. Alternative: storage nodes could be merged with compute nodes (min 3 worker nodes) but it could have impacts on performance.</td>
    </tr>
    <tr>
        <td> <strong>Type</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Primary Capability</strong> </td>
        <td>
            
                <div>container platform</div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Implementation</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Architectural Decision</strong> </td>
        <td>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_ryf2QV5mjSYF">Persistent Storage Options for Applications</a></div>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_ByJ2Q4q7jBKt">Storage Technology for Metrics & Logging</a></div>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_ByisXEcmoSKK">Storage Technology for Red Hat OpenShift Cluster Platform Registry</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Non Functional Requirement</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Generic Group</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Sub-level Diagram</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Related Diagrams</strong> </td>
        <td>
            
                <div><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></div>
            
                <div><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></div>
            
                <div><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></div>
            
                <div><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Related Elements</strong> </td>
        <td>
            
                <div>Persistent Storage Options for Applications</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                
            
                <div>Storage Technology for Metrics & Logging</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                
            
                <div>Storage Technology for Red Hat OpenShift Cluster Platform Registry</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                
            
            
                <div>container platform</div>
                
            
        </td>
    </tr>
</table>


</details>


    

<details markdown=1>
<summary markdown="span">Storage node 3</summary>

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
        <td>Storage node 3</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Storage for persistent volumes is embedded into the cluster and managed as containers. Some examples are:

Rook Ceph
Red Hat OpenShift Data Foundation   
Portworx

Dedication of storage nodes. Isolate storage workload on specific nodes. There are pods, deployed on the cluster that are managing access to storage resource. Alternative: storage nodes could be merged with compute nodes (min 3 worker nodes) but it could have impacts on performance.</td>
    </tr>
    <tr>
        <td> <strong>Type</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Primary Capability</strong> </td>
        <td>
            
                <div>container platform</div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Implementation</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Architectural Decision</strong> </td>
        <td>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_ByisXEcmoSKK">Storage Technology for Red Hat OpenShift Cluster Platform Registry</a></div>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_ryf2QV5mjSYF">Persistent Storage Options for Applications</a></div>
            
                <div><a href="../../Architectural Decisions/architecturaldecision_ByJ2Q4q7jBKt">Storage Technology for Metrics & Logging</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Non Functional Requirement</strong> </td>
        <td>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Generic Group</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Sub-level Diagram</strong> </td>
        <td></td>
    </tr>
    <tr>
        <td> <strong>Related Diagrams</strong> </td>
        <td>
            
                <div><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></div>
            
                <div><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></div>
            
                <div><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></div>
            
                <div><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></div>
            
                <div><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></div>
            
                <div><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></div>
            
        </td>
    </tr>
    <tr>
        <td> <strong>Related Elements</strong> </td>
        <td>
            
                <div>Storage Technology for Red Hat OpenShift Cluster Platform Registry</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                
            
                <div>Persistent Storage Options for Applications</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                
            
                <div>Storage Technology for Metrics & Logging</div>
                
                    
                    <li><a href="../../IT System View/aoditsystem_HJ4nuWvtF">08 Red Hat OpenShift on IBM Cloud on VPC</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rkfCxWPYY">09 Azure</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_HkaCNxvtF">07 AWS</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_Sy-F43rKt">06 Two clusters on two regions</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_rk9c-3BtF">05 Two clusters on-premises</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_ByreAoBFK">04 Cloud cluster</a></li>
                    
                    <li><a href="../../IT System View/aoditsystem_B1r5OjHFF">03 On-premises cluster</a></li>
                    
                
            
            
                <div>container platform</div>
                
            
        </td>
    </tr>
</table>


</details>


    



