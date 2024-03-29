# Airflow

_Last updated 2020-11-25 for Airflow-CWL 1.2.6 based on Apache Airflow 1.10.12_ 

| Documentation  | ✅ |
| How-Tos        | ✅ |
| Install guides | ✅ |
| GUI            | ✅ |
| CLI		 | ⚠️  |
| Demo		 | ❌ |
| Local install	 | ✅ |
| Cluster	 | ❌ |
| Cloud		 | ❌ |
| Complex setup	 | ⚠️  |
| Complex use	 | ⚠️  |
| CWL version	 | v1.1 |

🚧 - Work-in-progress  
✅ - Support  
❌ - No support  
⚠️  - Complicated  

## Overview

Related links:
* [Python Package](https://pypi.org/project/cwl-airflow/)
* [Airflow Documentation](https://airflow.apache.org/docs/stable/)
* [CWL-Airflow Documentation](https://cwl-airflow.readthedocs.io/en/latest/readme/how_to_use.html#using-airflow-cli)
* [Airflow](https://airflow.apache.org/)
* [CWL-Airflow Github](https://github.com/Barski-lab/cwl-airflow)

Airflow is  a platform to programmatically author, schedule and monitor workflows.  It is used to define and run workflows on a local machine. CWL-Airflow is an extension to this which supports the execution of CWL workflows.

## Documentation

> Documentation? Yes

Airflow itself has very detailed documentation which describes how to install and configure Airflow and how to run workflows.   The documentation for CWL Airflow is not as extensive - however it contains enough information to get you running a workflow. What is missing is how to move beyond execution of workflows on a single machine.

### How to guides

> How to guides? Yes

Airflow has a lot of how to guides on usage, although their documentation on CWL specific use is much more limited, giving you only enough to get started.

### Install Guides

> Install guides? Yes

Airflow and cwl-airflow require that you install a single python package. The documnetation helpfully details the external dependencies that are needed by the python package (mainly python headers and docker in some cases), as such it has only few install steps.

## Features

### GUI / Web interface

> GUI? Yes

Airflow has a web interface that may be used to submit, view and create various workflows. The web interface allows for the creation of DAGs (the primary way that Airflow defines workflows).  When running CWL workflows, users are required to write a short (less than 3 lines) DAG wrapper for their CWL workflows and as such the Airflow documentation applies directly to CWL workflows.  The web interface, and how to use it, is documented well in Airflow.  There are additional instructions for CWL specific aspects in the CWL Airflow documentation.

### Command Line

> Command Line? Indirect

Airflow is designed to have workflows triggered from the web UI.  They can however be triggered from the commandline using airflow.  Additional control for viewing the status and other features of the workflows can be found through the REST API.  However there is no fully functional native command line interface beyond the REST API.

### Demo

> Demonstration platform available? No

No

## Environment

### Single Machine

> Run on single machine? Yes

Airflow is designed to run on a single node.  It has a server and client component, but these are designed to be installed on a single machine.

### Cluster

> Run on cluster? No

No

### Cloud

> Run on cloud? No

No

## Installation

> Is the install process complex? No

Whilst only a single python package is required to install CWL-Airflow, there are a few configuration files that need to be edited, and directories that need creating for Airflow to run.  Additionally 3 different services need to be started so that worklows can be submitted and executed.

