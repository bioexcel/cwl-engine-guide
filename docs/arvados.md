
## Arvados

Arvados supports two main ways to be installed on a local machine.

* Arvados-in-a-box
* Single host install

[Arvados-in-a-box](https://doc.arvados.org/install/arvbox.html) is a docker based container. This uses a docker container to run an instance of Arvados on a machine.  This requires that the user have root privilages and docker installed.

The [Single host](https://doc.arvados.org/v2.1/install/salt-single-host.html) install of Arvados uses Saltstack to install and configure Arvados on the machine, as such this requires and installation and knowledge of Salt.  For teh purposes of testing locally this is perhaps better suited to those who plan to use the cluster install of Arvados (using Saltstack) later.  There is also the option to do a complete manual install of Arvados although they themselves note that this is complex.

For pure ease of install, Arvados-in-a-box would be the recommended way forward for a test and development environment.
# Cluster installation

## Arvados

Arvados can be configured for use on and with a cluster in 3 main ways:

* Using saltstack to setup and configure a cluster
* Setting up Arvados to wrok with a Kubernetes cluster
* Manual installation of Arvados and the cluster.




# Overview

## Arvados

Arvados provides 2 main ways to use it:

* Single user and single host install
* Multi-user cluster
