provider   "azurerm"   { 
   version   =   "= 2.0.0" 
   features   {} 
    subscription_id = "28e6d331-0880-443b-887b-c141106fbf31"
  client_id       = "05878008-cbb0-4080-b7a7-393c5833eb13"
  client_secret   = "50ba3a13-bb3b-4607-aebd-30b562802c1d"
  tenant_id       = "e901cf7d-2901-4fe9-875c-4c2ea13f1e10"
 } 
 resource   "azurerm_resource_group"   "rg"   { 
   name   =   "my-first-terraform-rg" 
   location   =   "northeurope" 
 } 
 resource   "azurerm_virtual_network"   "myvnet"   { 
   name   =   "my-vnet" 
   address_space   =   [ "10.0.0.0/16" ] 
   location   =   "northeurope" 
   resource_group_name   =   azurerm_resource_group.rg.name 
 } 

 resource   "azurerm_subnet"   "frontendsubnet"   { 
   name   =   "frontendSubnet" 
   resource_group_name   =    azurerm_resource_group.rg.name 
   virtual_network_name   =   azurerm_virtual_network.myvnet.name 
   address_prefix   =   "10.0.1.0/24" 
 } 
