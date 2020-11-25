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
