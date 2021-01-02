# AKS network Design and key resources

**SCOPE:** AKS netowkring within and outside of AKS including dependencies on DNS, Load balancers, Firewalls etc.

## Azure VNET/Subnets for AKS

The VNET and Subnets are created in advance before AKS is deployed.
The VNET/Subnets are created by network engineering in the 'Jb-Resource' subscription'.  The AKS-STAGE and AKS-PROD vnets however have been created in the Prod 2.0 subscription.  
NOTE: There is no cost implication for VNET resources.

** AKS VNET and Subnet pre-requisites

| ENV | vNet/Address | subnet/address | Id|
|     :---:    |     :---:      |     :---:      |   :---:     |
| DEV   | Aks-nprod-vn/10.124.176.0/20     | Aks-dev-subnet/10.124.176.0/21    |    :---:     |
| QA     | Aks-nprod-vn/10.124.176.0/20       | Aks-dev-subnet/10.124.176.0/21      |    :---:     |

## Certificates 
- where are they stored (TLS)
- where termination happens
- key args for NGINX (version)
- F5 -->APIM--AKS backend
- F5 -APIM -ASE--AKS
