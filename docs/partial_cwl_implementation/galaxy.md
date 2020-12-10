# Cromwell

_Last updated 2020-11-26 for Galaxy v20.09_

| Documentation  | ❌ |
| How-Tos        | ❌ |
| Install guides | ⚠️  |
| GUI            | ✅ |
| CLI		 | ️❌ |
| Demo		 | ❌ |
| Local install	 | ⚠️  |
| Cluster	 | ⚠️  |
| Cloud		 | ⚠️  |
| Complex setup	 | ️✅ |
| Complex use	 | ️✅ |
| CWL version	 | Unknown |

🚧 - Work-in-progress  
✅ - Support  
❌ - No support  
⚠️  - Complicated  

## Overview

Related links:
* [Galaxy Project](https://galaxyproject.org)
* [Galaxy Github](https://github.com/galaxyproject)
* [Galaxy Install Docs](https://galaxyproject.org/admin/get-galaxy/)
* [CWL Galaxy Source code](https://github.com/common-workflow-language/galaxy)
* [Galaxy on a Cluster Docs](https://training.galaxyproject.org/training-material/topics/admin/tutorials/connect-to-compute-cluster/tutorial.html)
* [Galaxy in the cloud](https://galaxyproject.org/cloud/)
Galaxy is a workflow language in its own right. As such support for CWL is secondary and manily provided through separate community support.

## Documentation

> Documentation? No

Galaxy has comprehensive documentation on how to use and install, but no documentation related to how to support or use CWL on galaxy.

### How to guides

> How to guides? No

Galaxy has good documentation but lacks any information on how to run a CWL workflows.


### Install Guides

> Install guides? Complicated, not obvious for CWL Galaxy

Galaxy has instructions to get Galaxy setup and installed, and this only requires a few steps.  The is no documentation available on how to configure Galaxy to support CWL
There is a galaxy with [CWL repository](https://github.com/common-workflow-language/galaxy) and the instructions to install galaxy from source can be used with this as the source code to install Galaxy, but no support is given.

## Features

### GUI / Web interface

> GUI? Yes


### Command Line

> Command Line? No


### Demo

> Demonstration platform available? No

## Environment

### Single Machine

> Run on a single machine? Yes

Galaxy by default will run on a single machine.

### Cluster

> Run on a cluster? Yes, but not clear if possible for CWL Galaxy

Galaxy can be configured to run on a cluster.  Training material on how to configure this is provided [here]((https://training.galaxyproject.org/training-material/topics/admin/tutorials\
/connect-to-compute-cluster/tutorial.html).  Again this is for Galaxy without CWL, but by using the CWL Galaxy repository an install may be possible.

### Cloud

> Run on the cloud? Yes, but not clear if possible for CWL Galaxy

Galaxy has instructions for how to install and deploy on the [loud](https://galaxyproject.org/cloud/). Whether this applies to CWL galaxy is unknown.

## Installing

> Is the install process complex? Yes

Installing Galaxy has few steps and good documentation.  It is not clear how to install CWL Galaxy and whether the same steps can be followed with the exception of changing the source repository to CWL Galaxy.