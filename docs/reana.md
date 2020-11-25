
---
title: Resources
---
Documentation? Yes
How to guides? Yes
Install Guides? Yes
GUI? Yes
CLI? Yes
Demo? No
Single Machine? Sort of (MiniKube)
Cluster? Yes (K8s)
Cloud? Indirectly (K8s)
Complexity to setup? Low
Complexity to use? ???


# Understanding REANA

https://docs.reana.io/
https://github.com/reanahub/reana-demo-helloworld



REANA is a platform for running workflows.  It features two main packages for a server and client.  The server provides a scheduler and nodes on which to run workflows.



Documentation? Yes/No

REANA has previously had very thorough documentation on both installation of the software and using it for a workflow.  However, at the time of writing this guide their documentation is under a major overhaul and re-write which has resulted in some areas to be lacking documentation - the titles are there but the content has not been re-written.  I would hope that the documentation will return to normal soon, but we cannot guarentee this nor know when this should happen.

Usage guides? Yes/No

Currently REANA has a very brief tutorial on how to submit and retrieve a workflow. There is enough information to get started, but the detailed tutorial has not been re-written yet.

Install Guides? Yes/No

There are two componenets to a REANA install: the command line client, and the server.  Both installations have only a few steps required to install them.

The commandline client is available as a python package. [Installation](http://docs.reana.io/getting-started/first-example/) is limitted to a `pip install` with the need to export the servers url and an access token.

The server installation has two sets of instructions, one for a local install and one for a cluster (or at scale) both require kubernetes.  The cluster of "at scale" install is done using helm on an kubernetes cluster - which means that it assumes the existence of a kubernetes cluster.

The local install requires the use of minikube to create a local single machine kubernetes cluster.  REANA provide [documentation](http://docs.reana.io/development/deploying-locally/) on how to install and setup minikube to provide a REANA instance on a single node or machine.

<!-- As with other documentation, this is short and to the point.  If the [installation](http://docs.reana.io/development/deploying-at-scale) works on your system then it is fine. However, if you encounter any problems the documentation is not detailed enough to work you through it at this time. -->


# Features

GUI? Yes/No

REANA include a minimalist and clear GUI through a web browser.  This can be used to view workflow history and status.

.. ? Can it be used to submit jobs? or Download? Diagram suggests yes!

CLI? Yes/No

REANA's preferred method for submitting and interacting with workflows is through the command line (which is written in python and can be installed using the python package manager `pip`). Documentation is provided on how to submit and interact with workflows.  Additionally example workflows and instructions on how to run them are provided allowing for better understanding of how the system works.


Demo? Yes/No

No.

Single Machine? Yes/No

Whilst REANA is designed to work with a cluster, the developers document clearly how to configure it to work on a single machine using kubernetes.  This does result in a lot of applications to install and the overhead of running these, but the process is quick and clear.

Cluster? Yes/No




REANA is designed to work with a cluster to provide the computing power and storage.  The preferred way of doing this is with a kubernetes cluster. 

Cloud? Yes/No

REANA does not have a native interface to AWS or other cloud providers.


<!-- Could we use a k8s on AWS?, but these could potentially be used as part of a kubernetes cluster. -->

# Installing

How complex?

REANA is designed to be deployed on a kubernetes cluster. The documentation provides details of how to deploy a REANA cluster using helm. There is no "common problems" section.  This maybe due to the simplicity of the install, or an oversight on the part of the development team - in which case, the documentation may improve as the re-write continues but currently it is very sparse and assumes no install problems.

