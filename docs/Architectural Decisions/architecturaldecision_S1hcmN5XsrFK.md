

# OCP-012

### Name

Container Registry

### Status

accepted

### Last Update

2022-03-03

### Subject Area

OCP-Platform

### Topic



### Issue or Problem Statement

Container Registry to use with Red Hat OpenShift. Consider requirements such as replication, or vulnerability scanning where Red Hat Platform Plus with Quay + Clair and Red Hat Advanced Cluster Security would provide better value for the design.

### Assumptions

<div>OpenShift provides a built-in container registry, but can also use Red Hat Quay (bundled with Red Hat OpenShift Platform Plus) or 3rd party container registries such as JFrog Artifactory or IBM Cloud Container registries.</div><div><br></div><div><br></div>

### Motivation

<a href="https://docs.openshift.com/container-platform/4.9/registry/index.html" target="_blank">https://docs.openshift.com/container-platform/4.9/registry/index.html</a>

### Notes



[Expand all](#){ .md-button .same-line }

### Alternatives


    

<details markdown=1>
<summary markdown="span">External registries</summary>

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
        <td>External registries</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>External registries are managed independently of the Red Hat OpenShift cluster and require authentication, scaling, and updates to be setup and managed separately.</td>
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
<summary markdown="span">Integrated Red Hat OpenShift container registry</summary>

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
        <td>Integrated Red Hat OpenShift container registry</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>The integrated registry runs as a standard workload leveraging security and management features including integrated authentication, auto-scaling, new image notification, and updates[^10.1].
https://docs.openshift.com/container-platform/4.9/networking/routes/route-configuration.html</td>
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
<summary markdown="span">Quay</summary>

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
        <td>Quay</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Quay is part of OpenShift Plus. 
https://www.redhat.com/en/resources/openshift-platform-plus-datasheet
https://www.redhat.com/en/technologies/cloud-computing/quay
https://www.redhat.com/en/resources/quay-datasheet</td>
    </tr>
    <tr>
        <td> <strong>Best Applied</strong> </td>
        <td>When customer has purchased OpenShinft Plus and needs additional security scanning. 
Some additional functionality that Quay provides, and may be part of the decision, include:
- More Granular Access Control based on external authentication providers - (LDAP, OAuth/OIDC, Keystone, etc.)
- Transport layer TLS security
- Security scanning of images
- Activity Logging 
- Time machine / Image rollback
- Geo-distribution</td>
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



