# Deploy Process of psiprivacy.org on Azure

This page describes the deployment of the PSI Privacy application on Azure.

(Note: Consult team for passwords/access. e.g. LastPass)

## Azure Cluster Creation

Using the Azure web console, a new Kubernetes Servcie was created with the following parameters:

1. Resource group: `OpenDP-ResourceGroup`
1. Cluster name: `OpenDP-Cluster01`
1. Node Size: `DS2_v2` (also shown as `Standard_DS2_v2`) - (2 CPUs, 7 GB RAM)
1. Node count: 2


### Create Static IP

1. Retrieve load balancer name
  ```
  az aks show --resource-group OpenDP-ResourceGroup --name OpenDP-Cluster01 --query nodeResourceGroup -o tsv
  ```
  - Resulting load balancer name: `MC_OpenDP-ResourceGroup_OpenDP-Cluster01_eastus`
    - May also be found on the web console, in the list of resources
2. Create the IP address
  ```
  az network public-ip create --resource-group MC_OpenDP-ResourceGroup_OpenDP-Cluster01_eastus --name openDP-PSI_Privacy-IP --sku Standard --allocation-method static --query publicIp.ipAddress -o tsv
  ```
  - resulting IP: `52.151.200.161`
3. Add IP to the   
