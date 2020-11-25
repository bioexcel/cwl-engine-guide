---
title: TOIL
---

Correct as of 25th November 2020

| Documentation | How-Tos | Install guides | GUI | CLI | Demo | Local install | Cluster | Cloud | Complex setup | Complex use | CWL version |
| -- | --- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| 🚧 | 🚧 | ✅ | ❌ | ✅ | ❌ | ⚠ | ✅ | ⚠ | ⚠ | ⚠ | v1.2.0-dev4 |


----


# Understanding Toil

Related links:
* [TOIL homepage](https://toil.ucsc-cgl.org/)
* [TOIL installation instructions](http://toil.readthedocs.io/en/latest/gettingStarted/install.html)
* [TOIL release notes](https://github.com/DataBiosphere/toil/releases/latest)
* [TOIL documentation](https://toil.readthedocs.io/en/latest/)
* [TOIL Gitter channel](https://gitter.im/bd2k-genomics-toil/Lobby)

Toil is a highly customisable workflow engine, written purely in python. It is a client side workflow engine only. It has multiple plugins which allow it to submit and control workflows.  Whilst some plugins are fully supported by the developers, others are considered to principally be community supported (including the toil plugin).  Through these plugins toil provides a single interface to access many different backends. 


## Documentation

Toil has clear documentation on how to install it and setup workflows. The documentation is thorough, although it is a little chaotic and hard to follow in places. Toil has its own native workflow system which dominates the documentation making it not as obvious to understand how to run a CWL workflow.  Toil is based heavily around interconnecting components. Whilst the documentation explains how to connect these together to run a toil workflow on various setups - it is not as clear how to use these with CWL, or how to run a CWL workflow the diverges from their singular use example.

## How to guides

These are limited, but enough to get started running a CWL workflow on a local machine or on AWS.

## Install Guides

Toil is a client based workflow system; as such it requires only a python package to be installed on the local machine (or submission host for HPC) and access to a cloud or HPC cluster to run. It can be installed from source or using pip or conda (via conda-forge), with documentation covering the options for installing via pip or building from source.

CWL support is provided by the cwltool, and can be added at install time simply using `pip install toil[cwl]` (or equivalent for your install system).

# Features

## GUI

None.

## CLI

Toil is a command line only client. Toil has various commands that allow you to get the status of the workflows or clusters it is running on.

## Demo

As Toil is a client only workflow engine, there is no demo.  There are install instructions and examples to get you started though.

## Single Machine

Toil is supported on linux and OSX systems (we have not tested it on windows, nor is this mentioned in the documentation).

Toil-cwl-runner will use toil to execute a CWL workflow and run it on the local machines - this is perhaps suitable for development and testing of workflows, but not for production workflows. It can use docker or singularity (still experimental) for running containers.


## Cluster

Toil is a client only workflow engine.  Various plugins allow users to submit jobs toeither HPC or Cloud systems.  Some are supported, and others are community support only.

## Cloud

Toil supports Amazon Web Services (AWS), Google Compute Engine (GCE), and Kubernetes (for Kubernetes it uses AWS as its job store). It manages jobs on these systems using Apache Mesos as the batch system. [Instructions are given in the documentation](https://toil.readthedocs.io/en/latest/running/cloud/cloud.html) for how to setup and use these systems.


# Installing

Toil is a client only workflow engine, and requires only a single python package to be installed.
     
Extra features?
REST API?
