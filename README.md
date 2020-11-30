# Code example using the 3scale toolbox Jenkins shared library

This repository holds an example to showcase the use of the 3scale toolbox Jenkins shared library to automate the delivery of APIs using CI/CD and more specifically Jenkins pipelines.

##  Demo story

We want to automate deployment of an API managed by 3scale across multiple environments, using pre-defined pipelines provided by the platform. The delivery pipelines must support environment-specific properties, testing, versioning, and the ability to rollback incomplete or failed deployments.
This demo is composed of the following components: 
**Products and Projects**

    • OpenShift Container Platform
    • Red Hat 3scale API Management
    • 3scale toolbox
    • Jenkins for CICD

### Prerequisites

The following instructions assuming that you are using OpenShift. But the same could be applied to Minishift as well. The demo requires these components:   
    • OpenShift Container Platform
    • Red Hat 3scale API Management: we are going to simulate two 3scale environments (development and test). An option can be the creation of two tenants (DEV,TEST) in a 3scale API Manager instance, another option is use two 3scale API Manager instances.
    • 3scale toolbox: find here the oficial 3scale toolbox image [3scale toolbox container image](https://catalog.redhat.com/software/containers/3scale-amp2/toolbox-rhel7/5d80bbe95a13461f5f050cf7).
    • Jenkins for CICD

A 3scale instance with two tenants: DEV and TEST or two 3scale instances. 


Find in this diagram the API lifecycle automation sequence flow 

![](doc_images/3scalecicddemo.png)
