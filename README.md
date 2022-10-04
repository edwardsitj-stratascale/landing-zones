# terraform-azurerm-app-lz

## Introduction

This terraform module will create the appropriate virutal network and subnets specified via input parameters. 

This will configure all of the logging and monitoring needed for those resources.

<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.3.0 |
| <a name="requirement_azurerm"></a> [azurerm](#requirement\_azurerm) | ~> 3.23 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_azurerm"></a> [azurerm](#provider\_azurerm) | 3.24.0 |
| <a name="provider_azurerm.hub"></a> [azurerm.hub](#provider\_azurerm.hub) | 3.24.0 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_name"></a> [name](#module\_name) | Azure/naming/azurerm | n/a |

## Resources

| Name | Type |
|------|------|
| [azurerm_monitor_diagnostic_setting.nsg](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/monitor_diagnostic_setting) | resource |
| [azurerm_monitor_diagnostic_setting.vnet](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/monitor_diagnostic_setting) | resource |
| [azurerm_network_security_group.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/network_security_group) | resource |
| [azurerm_resource_group.ssvc](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/resource_group) | resource |
| [azurerm_resource_group.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/resource_group) | resource |
| [azurerm_route_table.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/route_table) | resource |
| [azurerm_subnet_route_table_association.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/subnet_route_table_association) | resource |
| [azurerm_virtual_network.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/virtual_network) | resource |
| [azurerm_virtual_network_peering.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/virtual_network_peering) | resource |
| [azurerm_log_analytics_workspace.hub](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/log_analytics_workspace) | data source |
| [azurerm_monitor_diagnostic_categories.nsg](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/monitor_diagnostic_categories) | data source |
| [azurerm_monitor_diagnostic_categories.vnet](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/monitor_diagnostic_categories) | data source |
| [azurerm_subnet.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/subnet) | data source |
| [azurerm_virtual_network.hub](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/virtual_network) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_context"></a> [context](#input\_context) | The context of the resources.<br> Approved values include bizops, hub, sbx | `string` | `"sbx"` | no |
| <a name="input_environment"></a> [environment](#input\_environment) | The environment that the resources will be deployed in.<br> Approved values include dev, stg, prd | `string` | `""` | no |
| <a name="input_log_analytics_hub"></a> [log\_analytics\_hub](#input\_log\_analytics\_hub) | The central log analytics workpace name and resource group | `map(string)` | <pre>{<br>  "name": "law-us-hub-east2",<br>  "resource_group_name": "rg-us-mgsrvc-hub-east2"<br>}</pre> | no |
| <a name="input_region"></a> [region](#input\_region) | Region and region abbreviation (slug) | `map(string)` | <pre>{<br>  "name": "eastus2",<br>  "slug": "use2"<br>}</pre> | no |
| <a name="input_routes"></a> [routes](#input\_routes) | List of routes to be added to the evironment/context | `list(map(string))` | <pre>[<br>  {<br>    "address_prefix": "0.0.0.0/0",<br>    "name": "default",<br>    "next_hop_in_ip_address": "10.24.0.68",<br>    "next_hop_type": "VirtualAppliance"<br>  },<br>  {<br>    "address_prefix": "10.11.0.0/16",<br>    "name": "10-11-0-0-16-via-afw",<br>    "next_hop_in_ip_address": "10.24.0.68",<br>    "next_hop_type": "VirtualAppliance"<br>  },<br>  {<br>    "address_prefix": "10.2.0.0/16",<br>    "name": "10-2-0-0-16-via-afw",<br>    "next_hop_in_ip_address": "10.24.0.68",<br>    "next_hop_type": "VirtualAppliance"<br>  },<br>  {<br>    "address_prefix": "10.3.0.0/16",<br>    "name": "10-3-0-0-16-via-afw",<br>    "next_hop_in_ip_address": "10.24.0.68",<br>    "next_hop_type": "VirtualAppliance"<br>  },<br>  {<br>    "address_prefix": "172.16.17.0/24",<br>    "name": "vpn-172-16-17-0-24",<br>    "next_hop_in_ip_address": "10.24.0.68",<br>    "next_hop_type": "VirtualAppliance"<br>  }<br>]</pre> | no |
| <a name="input_subscription_app_id"></a> [subscription\_app\_id](#input\_subscription\_app\_id) | Subscription ID that you would like to deploy to | `string` | `"dbc1ee45-e4cf-4d5a-bf44-e975f4f2e7a5"` | no |
| <a name="input_subscription_hub_id"></a> [subscription\_hub\_id](#input\_subscription\_hub\_id) | The hub subscription ID | `string` | `"dbc1ee45-e4cf-4d5a-bf44-e975f4f2e7a5"` | no |
| <a name="input_tag_business_criticality"></a> [tag\_business\_criticality](#input\_tag\_business\_criticality) | TAG: BusinessCriticality | `string` | `"Low"` | no |
| <a name="input_tag_business_unit"></a> [tag\_business\_unit](#input\_tag\_business\_unit) | TAG: BusinessUnit | `string` | `"IT Operations"` | no |
| <a name="input_tag_cost_center"></a> [tag\_cost\_center](#input\_tag\_cost\_center) | TAG: CostCenter | `string` | `"IT-Ops"` | no |
| <a name="input_tag_data_class"></a> [tag\_data\_class](#input\_tag\_data\_class) | TAG: DataClass | `string` | `"General"` | no |
| <a name="input_tag_ops_team"></a> [tag\_ops\_team](#input\_tag\_ops\_team) | TAG: OpsTeam | `string` | `"Cloud Operations"` | no |
| <a name="input_tag_owner"></a> [tag\_owner](#input\_tag\_owner) | TAG: Owner | `string` | `"it-ops@rhoworld.com"` | no |
| <a name="input_vnet_dns_servers"></a> [vnet\_dns\_servers](#input\_vnet\_dns\_servers) | The DNS servers to be used with vNet. | `list(string)` | <pre>[<br>  "10.24.0.68"<br>]</pre> | no |
| <a name="input_vnet_hub"></a> [vnet\_hub](#input\_vnet\_hub) | The hub VNET for getting peering information | `map(string)` | <pre>{<br>  "name": "VNET-HUB-EASTUS2",<br>  "resource_group_name": "RG-NET-HUB-EastUS2"<br>}</pre> | no |
| <a name="input_vnets"></a> [vnets](#input\_vnets) | This variable object is the heart of the module. This always must be defined. | <pre>map(object({<br>    address_prefixes = string<br>    peer_to_hub      = bool<br>    subnets          = list(map(string))<br>  }))</pre> | <pre>{<br>  "dev": {<br>    "address_prefixes": "10.24.64.0/23",<br>    "peer_to_hub": false,<br>    "subnets": [<br>      {<br>        "cidr": "10.24.64.0/24",<br>        "name": "data"<br>      }<br>    ]<br>  },<br>  "prd": {<br>    "address_prefixes": "10.23.68.0/23",<br>    "peer_to_hub": false,<br>    "subnets": [<br>      {<br>        "cidr": "10.23.68.0/24",<br>        "name": "data"<br>      }<br>    ]<br>  },<br>  "stg": {<br>    "address_prefixes": "10.23.66.0/23",<br>    "peer_to_hub": false,<br>    "subnets": [<br>      {<br>        "cidr": "10.23.66.0/24",<br>        "name": "data"<br>      }<br>    ]<br>  }<br>}</pre> | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_network_security_groups"></a> [network\_security\_groups](#output\_network\_security\_groups) | List of network security groups created for each of the subnets |
| <a name="output_resource_group_net"></a> [resource\_group\_net](#output\_resource\_group\_net) | Resource group where the networking resources were created |
| <a name="output_resource_group_ssvc"></a> [resource\_group\_ssvc](#output\_resource\_group\_ssvc) | Shared services resource group where the logging and diagnostics resources were created |
| <a name="output_route_table"></a> [route\_table](#output\_route\_table) | Route table that was created along with it's respective routes |
| <a name="output_subnets"></a> [subnets](#output\_subnets) | List of all subnets that were created |
| <a name="output_subscription_app_id"></a> [subscription\_app\_id](#output\_subscription\_app\_id) | Subscription where the resources were created |
| <a name="output_subscription_hub_id"></a> [subscription\_hub\_id](#output\_subscription\_hub\_id) | Subscription ID used for the hub resources |
| <a name="output_tags"></a> [tags](#output\_tags) | All tags that were applied |
| <a name="output_virtual_networks"></a> [virtual\_networks](#output\_virtual\_networks) | Virtual Networks that were created |
| <a name="output_vnet_hub"></a> [vnet\_hub](#output\_vnet\_hub) | Hub Virtual Network |
| <a name="output_vnet_peerings"></a> [vnet\_peerings](#output\_vnet\_peerings) | Virtual Network Peerings |
<!-- END_TF_DOCS -->
