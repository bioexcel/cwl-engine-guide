
---
title: Resources
---

# About this guide

This aims to be a lightly opinionated guide to help you decide which implementation of [CWL](https://www.commonwl.org/) is best suited to your needs.  The opinions given here are based off the individual engines own claims and our experience with them.


## What engines are covered

We are only covering those workflow engines that are stable and in production, not those still being developed and lacking support or functionality. The ones we will consider are:

* [Arvados](https://arvados.org/)
* [Toil](http://toil.ucsc-cgl.org/)
* [CWL-Airflow](https://github.com/Barski-lab/cwl-airflow)
* [REANA](http://www.reana.io/)


## How to use this guide.

This guide is written from the point of view of features.  You can read the whole guide, or if certain features are of particular interest you can read just those sections.  In each section we shall cover each workflow engine and how it supports each feature.


<!-- ?Use case based? -->


# Operating system

The various CWL engines support multiple different Operating Systems.  Some support different operating systems for submitting jobs from running them, and we do our best to clarfiy this.

## Arvados

Arvados supports jobs being submitted from both Linux and Windows systems (and possibly OSX, although the authors have not tested, it should be possible).  This is done through the use of a commandline tool to interact with an Arvados.

.. cluster, single machine, or VM/Container (such as Arvados-in-a-box); and a web interface.

Arvados' documentation is geared towards uploading jobs and workflows through a GUI in the form of a webinterface. From here users can fully control and run their workflows.

The commandline tools to interact with Arvados and submit jobs are written in both Python and Ruby.  These can be installed through `pip` and `gems`.

<!--  The documentation on how to use these does not appear as comprehensive as the web interface, and is a little more diff -->


# Run on local machine, or single host

We discuss here whether each implementation can run on a local machine or single host. This is useful if you lack access to a cluster, or wish to develope your workflows on a single machine. For small workflows, the hastle of setting up a cluster maybe more time consuming that is needed for the workflow.


## Arvados

Arvados supports two main ways to be installed on a local machine.

* Arvados-in-a-box
* Single host install

[Arvados-in-a-box](https://doc.arvados.org/install/arvbox.html) is a docker based container. This uses a docker container to run an instance of Arvados on a machine.  This requires that the user have root privilages and docker installed.

The [Single host](https://doc.arvados.org/v2.1/install/salt-single-host.html) install of Arvados uses Saltstack to install and configure Arvados on the machine, as such this requires and installation and knowledge of Salt.  For teh purposes of testing locally this is perhaps better suited to those who plan to use the cluster install of Arvados (using Saltstack) later.  There is also the option to do a complete manual install of Arvados although they themselves note that this is complex.

For pure ease of install, Arvados-in-a-box would be the recommended way forward for a test and development environment.
# Cluster installation

## Arvados

Arvados can be configured for use on and with a cluster in 3 main ways:

* Using saltstack to setup and configure a cluster
* Setting up Arvados to wrok with a Kubernetes cluster
* Manual installation of Arvados and the cluster.




# Overview

## Arvados

Arvados provides 2 main ways to use it:

* Single user and single host install
* Multi-user cluster







## Recommended tutorials 

* <https://www.commonwl.org/user_guide/>
* <https://mmb.irbbarcelona.org/biobb/availability/tutorials/cwl>





##################################################################

New Format????


# Understanding
Documentation? Yes/No

How to guides? Yes/No

Install Guides? Yes/No

# Features

GUI? Yes/No

CLI? Yes/No

Demo? Yes/No

Single Machine? Yes/No

Cluster? Yes/No

Cloud? Yes/No

# Installing

How complex?



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

----


# Understanding Toil

Toil is a highly customisable workflow engine. Toil is a client side workflow enginer only. It has multiple plugins which allow it to submit and control workflows.  Whilst some plugins are fully supported, some are considered community supported.  Through these plugins toil provides a single interface to access many different backends. 


Documentation? Yes/No

Toil has clear documentation on how to install it and setup workflows. The documentation is thorough, although it is a little chaotic and hard to follow in places. Toil has its own native workflow system which dominates the documentation making it not as obvious to understand how to run a CWL workflow.  Toil is based heavily around interconnecting components. Whilst the documentation explains how to connect these together to run a toil workflow on various setups - it is not as clear how to use these with CWL, or how to run a CWL workflow the diverges from their singular use example.

How to guides? Yes/No
    
Limitted, but enough to get started running a CWL workflow on a local machine or on AWS.

Install Guides? Yes/No

Toil is a client based workflow system; as such it requires only a python package to be installed on the local machine (or submission host for HPC) and access to a cloud or HPC cluster to run.

.. Okay, works like ganga??  Single submission file from python, pick and choose plugns.  Hopefully little change needed to swap from SLURM to HTCondor for instance?

.. Not clear how you install Toil for CWL, is it same as toil?   My understanding is that toil has only a client, and then interacts with any system you have setup, not clear how to define that though.

# Features

GUI? Yes/No

No Command Line only.

CLI? Yes/No

Toil is a command line only client.  Toil has various commands that allow you to get the status of the workflows or clusters it is running on.

Demo? Yes/No

As Toil is a client only workflow engine, there is no demo.  There are install instructions and examples to get you started though.

Single Machine? Yes/No

Toil cwl-runner will use toil to execute a CWL workflow and run it on the local machines - this is perhaps suitable for development and testing of workflows, but not for production workflows.

.. CWL is intended to be used with a cloud provider, but has some support for a kuberneties cluster (still requires AWS for job store) through the use of minikuvbe this can be provisioned on a single machine. ??? Need to review how easy thsi is.

Cluster? Yes/No

Toil is a client only workflow engine.  Various plugins allow users to submit jobs toeither HPC or Cloud systems.  Some are supported, and others are community support only.  When using cloud services, AWS must be used for the filestore.

Cloud? Yes/No

Toil is a client only workflow engine.  Various plugins allow users to submit jobs toeither HPC or Cloud systems.  Some are supported, and others are community support only.  When using cloud services, AWS must be used for the filestore.

# Installing

Toil is a client only workflow engine, and requires only a single python package to be installed.
     
Extra features?
REST API?




# Understanding Airflow

## Overview

Airflow is a scheduler ran on a local machine.  It can run workflow on a  local machine, or with the neccessary packages and user accounts, it can schedule jobs to run on cloud providers such as k8s or AWS.


Documentation? Yes/No

Airflow has detailed documentation on how to use it and configure it to use cloud resources such as AWS and kubernetes - although this is less obvious.

How to guides? Yes/No

Airflow has a lot how to guides on how to use, although their documentation on CWL specific use if much more limited, but gives you enough to get started.

Install Guides? Yes/No

Airflow and cwl-airflow require that you install a python package. As such it requires few install steps, but there are a few potential problems you can run into, but the documenation provides examples and solution to problems. 

# Features

GUI? Yes/No

Airflow has a webinterface that may be used to submit, view and create various workflows (does this work with CWL?)

CLI? Yes/No

Airflow has a well documented API to interact with the system from the command line.  Users can also submit jobs from the command line as well.

Demo? Yes/No

No

Single Machine? Yes/No

Yes. Airflow is a single pip install and will run on a local machine.

Cluster? Yes/No

Cloud? Yes/No

Yes, through the correct extra packages to connect to the c;loud.

# Installing

How complex?


Cannot get basic example to work.  No useful errors.
