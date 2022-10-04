<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.3.0 |
| <a name="requirement_azurerm"></a> [azurerm](#requirement\_azurerm) | ~> 3.23 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_azurerm"></a> [azurerm](#provider\_azurerm) | 3.25.0 |
| <a name="provider_azurerm.hub"></a> [azurerm.hub](#provider\_azurerm.hub) | 3.25.0 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_name"></a> [name](#module\_name) | Azure/naming/azurerm | n/a |

## Resources

| Name | Type |
|------|------|
| [azurerm_key_vault_access_policy.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/key_vault_access_policy) | resource |
| [azurerm_key_vault_key.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/key_vault_key) | resource |
| [azurerm_monitor_diagnostic_setting.sub](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/monitor_diagnostic_setting) | resource |
| [azurerm_monitor_diagnostic_setting.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/monitor_diagnostic_setting) | resource |
| [azurerm_private_endpoint.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/private_endpoint) | resource |
| [azurerm_storage_account.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/storage_account) | resource |
| [azurerm_storage_account_customer_managed_key.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/storage_account_customer_managed_key) | resource |
| [azurerm_client_config.current](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/client_config) | data source |
| [azurerm_key_vault.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/key_vault) | data source |
| [azurerm_log_analytics_workspace.hub](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/log_analytics_workspace) | data source |
| [azurerm_monitor_diagnostic_categories.sub](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/monitor_diagnostic_categories) | data source |
| [azurerm_monitor_diagnostic_categories.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/monitor_diagnostic_categories) | data source |
| [azurerm_private_dns_zone.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/private_dns_zone) | data source |
| [azurerm_resource_group.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/resource_group) | data source |
| [azurerm_subnet.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/subnet) | data source |
| [azurerm_virtual_network.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/virtual_network) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_app_name"></a> [app\_name](#input\_app\_name) | n/a | `string` | `"diag"` | no |
| <a name="input_context"></a> [context](#input\_context) | n/a | `string` | `"sbx"` | no |
| <a name="input_environment"></a> [environment](#input\_environment) | n/a | `string` | `"dev"` | no |
| <a name="input_key_vault_hub"></a> [key\_vault\_hub](#input\_key\_vault\_hub) | n/a | `map(string)` | <pre>{<br>  "name": "KVRHOUSHUBEAST1",<br>  "resource_group_name": "RG-US-MGSRVC-HUB-EAST2"<br>}</pre> | no |
| <a name="input_log_analytics_hub"></a> [log\_analytics\_hub](#input\_log\_analytics\_hub) | n/a | `map(string)` | <pre>{<br>  "name": "law-us-hub-east2",<br>  "resource_group_name": "RG-US-MGSRVC-HUB-EAST2"<br>}</pre> | no |
| <a name="input_region"></a> [region](#input\_region) | n/a | `map(any)` | <pre>{<br>  "name": "eastus2",<br>  "slug": "use2"<br>}</pre> | no |
| <a name="input_resource_group_name"></a> [resource\_group\_name](#input\_resource\_group\_name) | n/a | `string` | `"RG-SBX-SSVC-USE2"` | no |
| <a name="input_storage_type"></a> [storage\_type](#input\_storage\_type) | Enter one or more approved values ["blob","dfs","file","queue","table","web"] | `list(any)` | <pre>[<br>  "blob",<br>  "dfs"<br>]</pre> | no |
| <a name="input_subnet_name"></a> [subnet\_name](#input\_subnet\_name) | Enter the VNET for the storage account private endpoint | `string` | `"DataSubnet"` | no |
| <a name="input_subscription_app_id"></a> [subscription\_app\_id](#input\_subscription\_app\_id) | n/a | `string` | `"dbc1ee45-e4cf-4d5a-bf44-e975f4f2e7a5"` | no |
| <a name="input_subscription_hub_id"></a> [subscription\_hub\_id](#input\_subscription\_hub\_id) | n/a | `string` | `"dbc1ee45-e4cf-4d5a-bf44-e975f4f2e7a5"` | no |
| <a name="input_tag_business_criticality"></a> [tag\_business\_criticality](#input\_tag\_business\_criticality) | n/a | `string` | `"Low"` | no |
| <a name="input_tag_business_unit"></a> [tag\_business\_unit](#input\_tag\_business\_unit) | n/a | `string` | `"IT Operations"` | no |
| <a name="input_tag_cost_center"></a> [tag\_cost\_center](#input\_tag\_cost\_center) | n/a | `string` | `"IT-Ops"` | no |
| <a name="input_tag_data_class"></a> [tag\_data\_class](#input\_tag\_data\_class) | n/a | `string` | `"General"` | no |
| <a name="input_tag_ops_team"></a> [tag\_ops\_team](#input\_tag\_ops\_team) | n/a | `string` | `"Cloud Operations"` | no |
| <a name="input_tag_owner"></a> [tag\_owner](#input\_tag\_owner) | n/a | `string` | `"it-ops@rhoworld.com"` | no |
| <a name="input_vnet"></a> [vnet](#input\_vnet) | Enter the VNET name and resource group the storage account private endpoint | `map(string)` | <pre>{<br>  "name": "VNET-SANDBOX-DEV-EASTUS2",<br>  "resource_group_name": "RG-NET-SANDBOX-EAST2",<br>  "subnet_name": "DataSubnet"<br>}</pre> | no |
| <a name="input_vnet_hub"></a> [vnet\_hub](#input\_vnet\_hub) | n/a | `map(string)` | <pre>{<br>  "name": "VNET-HUB-EASTUS2",<br>  "resource_group_name": "RG-NET-HUB-EastUS2"<br>}</pre> | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_private_dns_zones"></a> [private\_dns\_zones](#output\_private\_dns\_zones) | n/a |
| <a name="output_private_endpoints"></a> [private\_endpoints](#output\_private\_endpoints) | n/a |
| <a name="output_storage_account"></a> [storage\_account](#output\_storage\_account) | n/a |
<!-- END_TF_DOCS -->
