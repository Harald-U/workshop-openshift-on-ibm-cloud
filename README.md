![logo](images/os_logo.png)

[Red Hat OpenShift on IBM Cloud](https://cloud.ibm.com/docs/openshift?topic=openshift-why_openshift) is an extension of the IBM Cloud Kubernetes Service where IBM manages OpenShift Container Platform for you. 

With Red Hat OpenShift on IBM Cloud developers have a fast and secure way to containerize and deploy enterprise workloads in Kubernetes clusters. OpenShift clusters build on Kubernetes container orchestration that offers consistency and flexibility for your development lifecycle operations.

# Deploying Java Microservices to OpenShift on IBM Cloud

Note: In order to run this workshop, you need an [IBM Cloud account](https://cloud.ibm.com/registration).

This workshop demonstrates how to build a microservice with Java and how to deploy it to OpenShift on the IBM Cloud.

The microservice is kept as simple as possible, so that it can be used as a starting point for other microservices. The microservice has been developed with Java EE and [Eclipse MicroProfile](https://microprofile.io/).

There are [various ways to deploy applications to OpenShift](http://heidloff.net/article/deploying-open-liberty-microservices-openshift/). The options have different advantages and disadvantages which are explained in the following labs.

## Labs

This workshop has 7 labs and should take between 60 and 90 minutues to complete. Here is an [Overview video (1:41 mins)](https://youtu.be/8361HGR_O_s) on Youtube.

The first lab describes how to install all required prerequisites. In the easiest case this means accessing the IBM Cloud Shell.

<**OPTIONAL**>Lab 2 and 3 describe how to develop a microservice with Java EE and Eclipse MicroProfile and are useful if you are interested in coding.<**/OPTIONAL**>

The next four labs show four different ways to deploy applications to OpenShift with their pros and cons in this specific scenario:

| Option | Dockerfile | yaml Files | Java Build | Docker Build |
| - | - | - | - | - |
| Lab 4: Kubernetes-like | required | required | OpenShift | OpenShift |
| Lab 6: Existing Image  | not required  | not required | N/A | N/A |
| Lab 7: Git Repo | required  | not required | OpenShift | OpenShift |
| Lab 8: Source to Image | not required | not required | Desktop | OpenShift |

---

To continue with the workshop follow these steps:

1. **>> [Prerequisites](1-prereqs.md) <<**
1. [OPTIONAL: Running the Java microservice locally](2-docker.md)
1. [OPTIONAL: Understanding the Java implementation](3-java.md)
1. [Deploying to OpenShift via 'oc' CLI](4-openshift.md)
1. [Distributed logging with LogDNA and OpenShift on IBM Cloud](5-logdna-openshift.md)
1. [Deploying existing images to OpenShift](6-existing-image.md)
1. [Deployments of code in GitHub repos](7-github.md)
1. [Source to Image deployments](8-source-to-image.md)

