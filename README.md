# Code example using the 3scale toolbox Jenkins shared library

This repository holds code samples to showcase the use of the 3scale toolbox Jenkins shared library to automate the delivery of APIs using CI/CD and more specifically Jenkins pipelines.

##  Demo story

We want to automate deployment of an API managed by 3scale across multiple environments, using pre-defined pipelines provided by the platform. The delivery pipelines must support environment-specific properties, testing, versioning, and the ability to rollback incomplete or failed deployments.

### Prerequisites

This demo is composed of the following components: 

**Products and Projects**

    • OpenShift Container Platform
    • Red Hat 3scale API Management
    • 3scale toolbox
    • Jenkins for CICD
    
The following instructions assuming that you are using OpenShift. But the same could be applied to Minishift as well.
A 3scale instance with two tenants: DEV and TEST or two 3scale instances. 


Find in this diagram the API lifecycle automation sequence flow 

![](doc_images/3scalecicddemo.png)
