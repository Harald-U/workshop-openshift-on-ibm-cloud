# OpenShift on IBM Cloud Workshop

![logo](images/os_logo.png)

[Red Hat OpenShift on IBM Cloud](https://cloud.ibm.com/docs/openshift?topic=openshift-why_openshift) is an extension of the IBM Cloud Kubernetes Service where IBM manages OpenShift Container Platform for you. 

With Red Hat OpenShift on IBM Cloud developers have a fast and secure way to containerize and deploy enterprise workloads in Kubernetes clusters. OpenShift clusters build on Kubernetes container orchestration that offers consistency and flexibility for your development lifecycle operations.

## Deploying Java Microservices to OpenShift on IBM Cloud

Note: In order to run this workshop, you need an [IBM Cloud account](https://cloud.ibm.com/registration).

This workshop demonstrates how to build a microservice with Java and how to deploy it to OpenShift on the IBM Cloud.

The microservice is kept as simple as possible, so that it can be used as a starting point for other microservices. The microservice has been developed with Java EE and [Eclipse MicroProfile](https://microprofile.io/).

There are [various ways to deploy applications to OpenShift](http://heidloff.net/article/deploying-open-liberty-microservices-openshift/). The options have different advantages and disadvantages which are explained in the following labs.

## Labs

This workshop has 8 labs. It should take between 60 and 90 minutues to complete the workshop.

0. [Overview video (1:41 mins)](https://youtu.be/8361HGR_O_s)
1. [Installing prerequisites](1-prereqs.md)
2. [Optional: Running the Java microservice locally](2-docker.md)
3. [Optional: Understanding the Java implementation](3-java.md)
4. [Deploying to OpenShift via 'oc' CLI](4-openshift.md)
5. [Deploying existing images to OpenShift](5-existing-image.md)
6. [Deployments of code in GitHub repos](6-github.md)
7. [Source to Image deployments](7-source-to-image.md)


The first lab describes how to install all required prerequisites. In the easiest case this is only Docker Desktop and an image with all other tools.

Lab 2 and 3 describe how to develop a microservice with Java EE and Eclipse MicroProfile and are useful if you are interested in programming, hence **they are optional**.

The next four labs explain four different ways to deploy applications to OpenShift with their pros and cons in this specific scenario:

| Option | Dockerfile | yaml Files | Java Build | Docker Build |
| - | - | - | - | - |
| Lab 4: Kubernetes-like | required | required | OpenShift | OpenShift |
| Lab 5: Existing Image  | not required  | not required | N/A | N/A |
| Lab 6: Git Repo | required  | not required | OpenShift | OpenShift |
| Lab 7: Source to Image | not required | not required | Desktop | OpenShift |

