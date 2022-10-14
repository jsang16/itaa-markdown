

# OCP-005

### Name

Control Plane Deployment Topology

### Status

accepted

### Last Update

2022-03-03

### Subject Area

OCP-Platform

### Topic

Placement policies for OpenShift Control Plane

### Issue or Problem Statement

Where and how control plane should be deployed across MZR or regional zone on Red Hat OpenShift

### Assumptions

<br>

### Motivation

<a href="https://www.redhat.com/en/blog/meet-single-node-openshift-our-smallest-openshift-footprint-edge-architectures" target="_blank">https://www.redhat.com/en/blog/meet-single-node-openshift-our-smallest-openshift-footprint-edge-architectures</a>

### Notes



[Expand all](#){ .md-button .same-line }

### Alternatives


    

<details markdown=1>
<summary markdown="span">3-control plane nodes configuration</summary>

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
        <td>3-control plane nodes configuration</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>The redesign of Red Hat OpenShift 4.x and performance improvements of its components make up Red Hat OpenShift 4.x it is no longer necessary to run with more than (&gt;) 3 control plane nodes.
3 control plane nodes can support loss of one node.</td>
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
<summary markdown="span">More than 3-control plane nodes configuration</summary>

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
        <td>More than 3-control plane nodes configuration</td>
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
<summary markdown="span">Single Node Control Plane</summary>

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
        <td>Single Node Control Plane</td>
    </tr>
    <tr>
        <td> <strong>Description</strong> </td>
        <td>Single Node Control Plane - https://www.redhat.com/en/blog/meet-single-node-openshift-our-smallest-openshift-footprint-edge-architectures</td>
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



