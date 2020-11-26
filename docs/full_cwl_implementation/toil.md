# Toil

_Last updated 2020-11-26 for Toil 4.2.0_

| Documentation  | ✅ |
| How-Tos        | 🚧 |
| Install guides | ✅ |
| GUI            | ❌ |
| CLI		 | ️✅ |
| Demo		 | ❌ |
| Local install	 | ✅ |
| Cluster	 | ✅ |
| Cloud		 | ✅ |
| Complex setup	 | ️✅️ |
| Complex use	 | ️⚠️  |
| CWL version	 | v1.2.0-dev4 |

🚧 - Work-in-progress  
✅ - Support  
❌ - No support  
⚠️  - Complicated  

## Overview

Related links:
* [Toil homepage](https://toil.ucsc-cgl.org/)
* [Toil installation instructions](http://toil.readthedocs.io/en/latest/gettingStarted/install.html)
* [Toil release notes](https://github.com/DataBiosphere/toil/releases/latest)
* [Toil documentation](https://toil.readthedocs.io/en/latest/)
* [Toil Gitter channel](https://gitter.im/bd2k-genomics-toil/Lobby)

Toil is a highly customisable workflow engine, written purely in python. It is a client side workflow engine only. It has multiple plugins which allow it to submit and control workflows.  Whilst some plugins are fully supported by the developers, others are considered to principally be community supported (including the toil plugin).  Through these plugins toil provides a single interface to access many different backends. 


## Documentation

> Documentation? Yes

Toil has clear documentation on how to install it and setup workflows. The documentation is thorough, although it is a little chaotic and hard to follow in places. Toil has its own native workflow system which dominates the documentation making it not as obvious to understand how to run a CWL workflow.  Toil is based heavily around interconnecting components. Whilst the documentation explains how to connect these together to run a toil workflow on various setups - it is not as clear how to use these with CWL, or how to run a CWL workflow the diverges from their singular use example.

### How to guides

> How to guides? Limited

These are limited, but enough to get started running a CWL workflow on a local machine or on AWS.

### Install Guides

> Install guides? Yes

Toil is a client based workflow system; as such it requires only a python package to be installed on the local machine (or submission host for HPC) and access to a cloud or HPC cluster to run. It can be installed from source or using pip or conda (via conda-forge), with documentation covering the options for installing via pip or building from source.


## Features

### GUI / Web interface

> GUI? No

None.

### Command Line

> Command Line? Yes

Toil is a command line only client. Toil has various commands that allow you to get the status of the workflows or clusters it is running on.

### Demo

> Demonstration platform available? No

As Toil is a client only workflow engine, there is no demo.  There are install instructions and examples to get you started though.

## Environment

### Single Machine

> Run on a single machine? Yes

Toil is supported on linux and OSX systems (we have not tested it on windows, nor is this mentioned in the documentation).

Toil-cwl-runner will use toil to execute a CWL workflow and run it on the local machines - this is perhaps suitable for development and testing of workflows, but not for production workflows. It can use docker or singularity (still experimental support, but more suitable for HPC environments) for running containers.

### Cluster

> Run on a cluster? Yes

Toil is a client only workflow engine.  Various plugins allow users to submit jobs to either HPC or Cloud systems.  Some are directly supported by developers, and others are principally community supported.

### Cloud

> Run on the cloud? Yes

Toil supports Amazon Web Services (AWS), Google Compute Engine (GCE), and Kubernetes (for Kubernetes it uses AWS as its job store). It manages jobs on these systems using Apache Mesos as the batch system. [Instructions are given in the documentation](https://toil.readthedocs.io/en/latest/running/cloud/cloud.html) for how to setup and use these systems.

## Installing

> Is the install process complex? No

Toil is a client only workflow engine, and requires only a few python packages to be installed. CWL support is provided by the cwltool, and can be added at install time simply using `pip install toil[cwl]` or `conda install toil cwltool` (or equivalent for your install system).
     
