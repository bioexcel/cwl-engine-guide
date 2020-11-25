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
