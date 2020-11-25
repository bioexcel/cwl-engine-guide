---
layout: default
title: About this guide
---

# About this guide

This BioExcel Best Practice Guide aims to be a lightly opinionated guide to help you decide which implementation of [CWL](https://www.commonwl.org/) is best suited to your needs.  The opinions given here are based off the individual engines own claims and our experience with them.

## Overview of Common Workflow Language

For an introduction to [Common Workflow Language](https://www.commonwl.org/), see:

* [CWL user guide](https://www.commonwl.org/user_guide/)

[BioExcel Best Practice Guides](https://docs.bioexcel.eu/) include:

* [Creating workflows with Common Workflow Language](https://docs.bioexcel.eu/cwl-best-practice-guide/)

## How to use this guide.

This guide is written from the point of view of features.  You can read the whole guide, or if certain features are of particular interest you can read just those sections.  In each section we shall cover each workflow engine and how it supports each feature.

## What engines are covered

We are only covering those workflow engines that are stable and in production, not those still being developed and lacking support or functionality. The ones we will consider are:

* [Toil](toil.md) - command line tool driven, can connect to multiple cloud/cluster compute backends
* [cwltool](https://github.com/common-workflow-language/cwltool) - reference implementation, only local execution
* [Arvados](arvados.md) - client/server with Web interface and CLI
* [CWL-Airflow](airflow.md) - extends Apache Airflow with CWL support
* [REANA](reana.md) - Kubernetes execution, CWL is one of the supported languages

No single workflow engine is the right for every user. We recommend you explore the engines according to this guide in the order prescribed above.

The [CWL list of implementations](https://www.commonwl.org/#Implementations) also include partial CWL implementations that can be considered for more specialist use cases, e.g. [CWLEXEC](https://github.com/IBMSpectrumComputing/cwlexec) for IBM Spectrum LSF customers.

