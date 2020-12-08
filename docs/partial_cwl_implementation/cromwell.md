# Cromwell

_Last updated 2020-11-26 for Toil 4.2.0_

| Documentation  | ❌ |
| How-Tos        | ❌ |
| Install guides | ❌ |
| GUI            | ❌ |
| CLI		 | ️✅ |
| Demo		 | ❌ |
| Local install	 | ✅ |
| Cluster	 | ✅ |
| Cloud		 | ✅ |
| Complex setup	 | ️️❌ |
| Complex use	 | ️✅ |
| CWL version	 | Partial 1.0 |

🚧 - Work-in-progress  
✅ - Support  
❌ - No support  
⚠️  - Complicated  

## Overview

Related links:
* [Cromwell homepage / Documentation](https://cromwell.readthedocs.io/en/stable/)
* [Cromwell Github](https://github.com/broadinstitute/cromwell)
* [Cromwell Tutorials](https://cromwell.readthedocs.io/en/stable/tutorials/FiveMinuteIntro/)

Cromwell is a highly customisable workflow engine written in Java.  It is a client side workflow engine - it does have a server option, but this is still more client side than a true server setup.  CWL is not full support in Cromwell.  Its primary langauge is WDL (Workflow Description Language).  Cromwell has implemented support for the most commonly used parts of CWL - and is active in implementing further parts of the specification when requested.  


## Documentation

> Documentation? No

Cromwell has very comprehenive docuemntation for how to use it with WDL (although the documentation is often chaotic and not clear where to begin) but lacks any information on how to run CWL job.

### How to guides

> How to guides? No

Cromwell has large amounts of documentation but lacks any information on how to run a CWL job.


### Install Guides

> Install guides? Yes

Cromwell is a command line client so it does not require any installation.  Even the server setup does not require any installation.  All that is needed is to have Java install on the machine/


## Features

### GUI / Web interface

> GUI? No, but REST API is available

Cromwell does not have a GUI, but does have web interface for REST API commands.

### Command Line

> Command Line? Yes

Cromwell is command line client.  Jobs can be submitted from the commandline.  As these are ran as commands and not submitted, there is no ability to question the status of the job.  When ran as a server, the REST API can be used to query the status of the workflow.

### Demo

> Demonstration platform available? No

## Environment

### Single Machine

> Run on a single machine? Yes

Cromwell, by default, runs on a local machine, as long as Java is available.

### Cluster

> Run on a cluster? Yes

Cromwell is a client workflow engine.  Various plugins allow users to submit jobs to either HPC or Cloud systems.

### Cloud

> Run on the cloud? Yes

Cromwell offers plugins to support various cloud providers such as: Amazon Web Services (AWS), Google Compute Engine (GCE), and Kubernetes.

## Installing

> Is the install process complex? No

Cromwell is a client only workflow engine, and requires only Java to be installed. 