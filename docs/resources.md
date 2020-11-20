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


? Use case based?

# Operation system

The various CWL engines support multiple different Operating Systems.  Some support different operating systems for submitting jobs from running them, and we do our best to clarfiy this.

## Arvados

Arvados supports jobs being submitted from both Linux and Windows systems (and possibly OSX, although the authors have not tested this, it should be possible).  This is done through the use of a commandline tool to interact with an Arvados cluster, single machine, or VM/Container (such as Arvados-in-a-box); and a web interface.

Arvados' documentation is geared towards uploading jobs and workflows through a GUI in the form of a webinterface. From here users can fully control and run their workflows.

The commandline tools to interact with Arvados and submit jobs are written in both Python and Ruby.  These can be installed through `pip` and `gems`.

.. The documentation on how to use these does not appear as comprehensive as the web interface, and is a little more diff


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
[O
How complex?



# Understanding ===== REANA

Documentation? Yes/No

REANA has previously had very thorough documentation on both installation of the software and using it for a workflow.  However, at the time of writing this guide their documentation is under a major overhaul and re-write which has resulted in some areas to be lacking documentation - the titles are there but teh content has not been re-written.  I expect that the documentation will return to normal soon, but we cannot guarentee this nor know when this should happen.

Usage guides? Yes/No

Currently REANA has a very brief tutorial on how to submit and retrieve a workflow. There is enough information to get started, but the detailed tutorial has not been re-written yet.

Install Guides? Yes/No

As with other documentation, this is short and to teh point.  If the installation works on your system then it is fine. However, if you encounter any problems the documentation is not detailed enough to work you through it at this time.


# Features

GUI? Yes/No

REANA include a minimalist and clear GUI through a web browser.  This can be used to view workflow history and status.

? Can it be used to submit jobs? or Download? Diagram suggests yes!

CLI? Yes/No

REANA uses a python library to provide its command line interface.  This can be installed using pip and needs only two additional pieces of informationt to configure it:

* The URL to a REANA cluster
* An access token for said cluster.

# Setup

Demo? Yes/No

No?

Single Machine? Yes/No

Whilst REANA is designed to work with a cluster, the developers document clearly how to configure it to work on a single machine using kubernetes.  This does result in a lot of applications to install and teh overhead of running these, but the process is quick and clear.

Cluster? Yes/No

REANA is designed to work with a cluster to provide teh computing power and storage.  The preferred way of doing this is with a kubernetes cluster. 

Cloud? Yes/No

REANA does not have a native interface to AWS or other cloud providers, but these could potentially be used as part of a kubernetes cluster.

# Installing

How complex?

REANA is designed to be deployed on a kubernetes cluster. The documentation provides brief details of how to deploy a REANA cluster using helm.  This documentation may improve as the re-write continues but it is very sparse and too the point at the time of writing this guide.


# Understanding ==== Toil

Documentation? Yes/No

Toil has clear documentation on how to install it and setup workflows. The documentation is thorough, although it is a little chaotic and hard to follow in places. Toil has its own native workflow system which dominates the documentation making it not as obvious to understand hwo to run a CWL workflow.

How to guides? Yes/No

Limitted, but enough to get started running a CWL workflow or setting up a cluster.


Install Guides? Yes/No

# Features

GUI? Yes/No

No Command Line only.

CLI? Yes/No

This is the only way to use toil.   It is not the easiest workflow engie to get job statuss from, but it is not diffcult.

Demo? Yes/No

Their is no demonstartion system; however you can use the toil cwl runner without a cluster or further setup to see if your job works.

Single Machine? Yes/No

Yes via CWL runner, or minikube.   The runner will use toil to execute a CWL workflow and run it on the local machines - this is perhaps suitable for development and testing of workflows.

CWL is intended to be used with a cloud provider, but has some support for a kuberneties cluster (still requires AWS for job store) through the use of minikuvbe this can be provisioned on a single machine. ??? Need to review how easy thsi is.

Cluster? Yes/No

Toil is designed to run workflows on an AWS or  Google Cloud.  The setup for these is relativly quick, and toil will configure the nodes for you.  A kubernetes cluster can be used for toil - however, the job store (which is needed to store outputs and inputs) has to be AWS.

Additionally, toil can be configured to use an HTCondor or other HPC environment but this is considered community supported.

Cloud? Yes/No

Yes.  This is the native way of running on toil

# Installing

How complex?

As toil provisions all the nodes on a cloud service for you, setup is straight forwared.  If this is being used on a cluster, then it is community supported and not as simple as no official documentation is provided.

Extra features?
REST API?




# Understanding ========= Airlow

Overview

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
[O
How complex?


Cannot get basic example to work.  No useful errors.