# Deploy Process of psiprivacy.org on Azure

This page describes the deployment of the PSI Privacy application on Azure.

(Note: Consult team for passwords/access. e.g. LastPass)

## Azure Cluster Creation

Using the Azure web console, a new Kubernetes Servcie was created with the following parameters:

1. Resource group: `OpenDP-ResourceGroup`
1. Cluster name: `OpenDP-Cluster01`
1. Node Size: `DS2_v2` (also shown as `Standard_DS2_v2`) - (2 CPUs, 7 GB RAM)
1. Node count: 2

Resulting load balancer name: `MC_OpenDP-ResourceGroup_OpenDP-Cluster01_eastus`

