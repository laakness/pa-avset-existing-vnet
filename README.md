# pa-avset-existing-vnet
Palo Alto Networks ARM template for deploying a pair of VM series firewalls in an Availability Set to an existing VNET using a single Resource Group

Some organizations may already have Azure resources deployed to an existing VNET.  This ARM template allows you to introduce new firewalls without
VNET peering.  After you configure your firewalls you can apply Route Tables (UDR) for egress traffic.

### Prerequisites
Active Azure subscription

Three subnets in your existing VNET for mgmt, untrust, and trust

### Powershell

Deploy the ARM Template
```
deploy.ps1 -subscriptionId "<subscription ID>" -resouceGroupName "new-or-existing-rg" -resourceGroupLocation "northcentralus" -deploymentName "mydeploy" templateFilePath azureDeploy.avset.json -parametersFilePath azureDeploy.parameters.avset.json
```

### Vendor Docs
[Palo Alto Azure Reference Architecture](https://www.paloaltonetworks.com/resources/whitepapers/intelligent-architectures-azure-reference-architecture)


### To do
Update the documentation/examples more
