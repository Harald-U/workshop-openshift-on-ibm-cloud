# Lab 6 - Deployments of Code in GitHub Repos

> Deployments of code in GitHub repos: [video (3:52 mins)](https://youtu.be/b3upMuZOpsY)

## Overview

This lab shows how to deploy applications from Git repositories. 

This deployment option checks whether a Dockerfile exist. With the Dockerfile a build on OpenShift is initiated. Since we use a Dockerfile with two stages, both the Java code is built as well as the Docker image.

Note that the yaml files are ignored with this approach.

Read the [documentation](https://docs.openshift.com/enterprise/3.0/dev_guide/new_app.html#specifying-source-code) for more details.

### Step 1

Make sure you are using your own project:

```
$ oc project
```

### Step 2

Create a new application and refer to the GitHub repo of this workshop and to a subdirectory (deploying-to-openshift) within the repo:

```
$ oc new-app https://github.com/Harald-U/workshop-openshift-on-ibm-cloud --context-dir=deploying-to-openshift --name=authors-git
```

As result you'll get this output.

<kbd><img src="images/lab-6-step-2-1.png" /></kbd>

Notice how OpenShift creates a number of Kubernetes and OpenShift objects without you having to create any yaml files. Port 3000 is read from the Dockerfile.

A build will be triggered and run on OpenShift.

<kbd><img src="images/lab-6-step-2-2.png" /></kbd>

After successful build, the pod and the service will be deployed. Note that the healthchecks defined in the yaml file are missing, since the yaml files are not used. Instead OpenShift uses intelligent defaults for as many settings as possible. 

<kbd><img src="images/lab-6-step-2-3.png" /></kbd>

### Step 3

In the last step create a route.

```
$ oc expose svc/authors-git
$ oc get route/authors-git
```

To test the deployment, append '/openapi/ui' to the URL in the output of 'oc get route/authors-git' and open it in a browser.

This is the deployed application with the route.

<kbd><img src="images/lab-6-step-3.png" /></kbd>

---

__Continue with [Lab 7 - Source to Image Deployments](./7-source-to-image.md)__
