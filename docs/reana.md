
---
title: REANA
---

| Documentation | How-Tos | Install guides | GUI | CLI | Demo | Local install | Cluster | Cloud | Complex setup | Complex use |
| -- | --- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| ⚠ | ⚠ | ✅ | ✅ | ✅ | ❌ | ⚠ | ✅ | ⚠ | ⚠ | ⚠ |


# Understanding REANA

Related links: 
* [REANA home page](https://reana.io)
* [REANA Documentation](https://docs.reana.io/) (client)
* [REANA deployment documentation](http://docs.reana.io/development/)
  - [Deploying locally](http://docs.reana.io/development/deploying-locally/)
  - [Deploying with Kubernetnes/Helm cluster](http://docs.reana.io/development/deploying-at-scale/)
* [Hello world example](https://github.com/reanahub/reana-demo-helloworld)
* [REANA-Workflow-Engine-CWL src](https://github.com/reanahub/reana-workflow-engine-cwl)
* [REANA-Workflow-Engine-CWL developer docs](https://reana-workflow-engine-cwl.readthedocs.io/en/latest/)
* [REANA-Workflow-Engine-CWL Docker images](https://hub.docker.com/r/reanahub/reana-workflow-engine-cwl)
* [REANA-Workflow-Engine-CWL issue tracker](https://github.com/reanahub/reana-workflow-engine-cwl/issues)
* [REANA-Workflow-Engine-CWL releases](https://github.com/reanahub/reana-workflow-engine-cwl/releases)
* [REANA Gitter chat room](https://gitter.im/reanahub/reana)

REANA is a platform for running workflows.  It features two main packages for a server and client.  The server provides a scheduler and nodes on which to run workflows.

REANA is a general workflow engine that can run both [CWL](https://commonwl.org/) and [Yadage](https://github.com/yadage/yadage) workflows, through an outer job submission in the form of a [reana.yml](http://docs.reana.io/reference/reana-yaml/) file that combines the CWL workflow file with the input files and desired output locations.

## Documentation

* Documentation? Yes/No

REANA previously had very thorough documentation on both installation of the software and using it for a workflow.  However, at the time of writing this guide (2020-12) their documentation is undergoing a major overhaul and re-write, which has resulted in some areas to be lacking documentation - the [titles are there](http://docs.reana.io/running-workflows/executing-workflows/) but the content has not been re-written.  We would hope that the documentation will return to normal soon, but we cannot guarentee this, nor know when this should happen.

## Usage guides

* Usage guides? Yes/No

Currently REANA has a very [brief tutorial](http://docs.reana.io/getting-started/first-example/) on how to submit and retrieve a workflow. There is enough information to get started, but the detailed tutorial has not been re-written yet.

## Install guides

There are two componenets to a REANA install: the command line client, and the server.  Both installations have only a few steps required to install them.

The [commandline client](https://reana-client.readthedocs.io/en/latest/) is available as a Python package. [Installation](http://docs.reana.io/getting-started/first-example/) is limitted to a `pip install` with the need to export the servers url and an access token. It is recommended to use a Python [virtualenv](https://docs.python-guide.org/dev/virtualenvs/) to ensure the REANA dependency versions do not clash with other Python applications installed.

The client communicates with a REANA server. The CLI documentation may assume you have access to an existing REANA install. 

The server installation has two sets of instructions, one for a local install and one for a cluster (or at scale) both require [Kubernetes](https://kubernetes.io/).  The cluster of "at scale" install is done using [helm](https://helm.sh/) on an Kubernetes cluster - which means that it assumes the existence of a Kubernetes cluster.

The [local install of REANA](http://docs.reana.io/development/deploying-locally) requires the use of _minikube_ to create a local single machine Kubernetes cluster.  REANA provide [documentation](http://docs.reana.io/development/deploying-locally) on how to install and setup minikube to provide a REANA instance on a single node or machine.

Knowledge about installing Kubernetes and associated technologies are essential to manage a production instance of REANA. The REANA install guide recommends:

* <https://docs.docker.com/engine/install/>
* <https://kubernetes.io/docs/tasks/tools/install-kubectl/>
* <https://kind.sigs.k8s.io/docs/user/quick-start/>
* <https://helm.sh/docs/intro/install/>

<!-- As with other documentation, this is short and to the point.  If the [installation](http://docs.reana.io/development/deploying-at-scale) works on your system then it is fine. However, if you encounter any problems the documentation is not detailed enough to work you through it at this time. -->


## Features

## GUI

REANA include a minimalist and clear GUI through a web browser.  This can be used to view workflow history and status.

<!-- . ? Can it be used to submit jobs? or Download? Diagram suggests yes! -->

## CLI

* CLI? Yes

REANA's preferred method for submitting and interacting with workflows is through the `reana-client` command line (which is written in Python and can be installed using the Python package manager `pip`). Documentation is provided on how to submit and interact with workflows.  Additionally example workflows and instructions on how to run them are provided allowing for better understanding of how the system works.

The [REANA-Client](https://reana-client.readthedocs.io/en/latest/) explains the command line options.

## Demo

* Demo? No

No demo is available, however the [Hello world example](https://github.com/reanahub/reana-demo-helloworld) provides a walk-through.

Some of the documentation assumes you have access to the <https://reana.cern.ch/> instance hosted by CERN - installing the REANA server locally is a 

## Single machine

* Single Machine? Local cluster

Whilst REANA is designed to work with a cluster, the developers document clearly how to configure it to work on a single machine using kubernetes.  This does result in a lot of applications to install and the overhead of running these, but the process is quick and clear.

## Cluster?

* Cluster? Yes (Kubernetes)


REANA is designed to work with a cluster to provide the computing power and storage.  The preferred way of doing this is with a kubernetes cluster. 

## Cloud

* Cloud? Indirectly

REANA does not have a native interface to deploy instances with AWS or other cloud providers, but Kubernetes clusters are frequently deployed on the cloud, and [AWS support Kubernetes](https://aws.amazon.com/kubernetes/).


<!-- Could we use a k8s on AWS?, but these could potentially be used as part of a kubernetes cluster. -->

# Installing

REANA is designed to be deployed on a Kubernetes cluster that is long-running with a fixed number of instances. 

The documentation provides details of how to deploy a REANA cluster using _helm_. There is no "common problems" section.  This maybe due to the simplicity of the install, or an oversight on the part of the development team - in which case, the documentation may improve as the re-write continues but currently it is very sparse and assumes no install problems.

