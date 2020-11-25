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




# Installing

How complex?


Cannot get basic example to work.  No useful errors.
