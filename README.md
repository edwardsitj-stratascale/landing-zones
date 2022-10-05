<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_azurerm"></a> [azurerm](#requirement\_azurerm) | = 3.23.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_azurerm"></a> [azurerm](#provider\_azurerm) | 3.23.0 |
| <a name="provider_azurerm.hub"></a> [azurerm.hub](#provider\_azurerm.hub) | 3.23.0 |
| <a name="provider_azurerm.sponsor"></a> [azurerm.sponsor](#provider\_azurerm.sponsor) | 3.23.0 |
| <a name="provider_random"></a> [random](#provider\_random) | 3.4.3 |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [azurerm_data_factory_integration_runtime_azure.data_factory_managed_integration_runtime](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/data_factory_integration_runtime_azure) | resource |
| [azurerm_key_vault_access_policy.key_vault_access_policy_adf](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_access_policy) | resource |
| [azurerm_key_vault_access_policy.key_vault_access_policy_managed_identity](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_access_policy) | resource |
| [azurerm_key_vault_access_policy.key_vault_access_policy_postgresql](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_access_policy) | resource |
| [azurerm_key_vault_key.key_vault_key_data_factory](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_key) | resource |
| [azurerm_key_vault_key.key_vault_key_postgresql](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_key) | resource |
| [azurerm_key_vault_key.key_vault_key_storage_account](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_key) | resource |
| [azurerm_key_vault_secret.key_vault_secret_accounting_password](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_secret) | resource |
| [azurerm_key_vault_secret.key_vault_secret_adf_password](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_secret) | resource |
| [azurerm_key_vault_secret.key_vault_secret_file_share_password](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_secret) | resource |
| [azurerm_key_vault_secret.key_vault_secret_postgresql_password](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_secret) | resource |
| [azurerm_key_vault_secret.key_vault_secret_psql_adf_orca](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_secret) | resource |
| [azurerm_key_vault_secret.key_vault_secret_psql_devops_orca](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_secret) | resource |
| [azurerm_key_vault_secret.key_vault_secret_psql_spotfire_activation_enrollment](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_secret) | resource |
| [azurerm_key_vault_secret.key_vault_secret_psql_spotfire_clin_ops_reports](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_secret) | resource |
| [azurerm_key_vault_secret.key_vault_secret_rws_api_password](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_secret) | resource |
| [azurerm_key_vault_secret.key_vault_secret_smdb_password](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_secret) | resource |
| [azurerm_key_vault_secret.key_vault_secret_spotfire_password](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_secret) | resource |
| [azurerm_key_vault_secret.key_vault_secret_spotfire_password_2](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_secret) | resource |
| [azurerm_key_vault_secret.key_vault_secret_stafftrack_password](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/key_vault_secret) | resource |
| [azurerm_monitor_action_group.action_group](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/monitor_action_group) | resource |
| [azurerm_monitor_diagnostic_setting.data_factory_diagnostic](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/monitor_diagnostic_setting) | resource |
| [azurerm_monitor_diagnostic_setting.postgresql_diagnostic](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/monitor_diagnostic_setting) | resource |
| [azurerm_monitor_metric_alert.data_factory_metric_alert](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/monitor_metric_alert) | resource |
| [azurerm_postgresql_server.postgresql](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/postgresql_server) | resource |
| [azurerm_postgresql_server_key.postgresql_encryption](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/postgresql_server_key) | resource |
| [azurerm_private_endpoint.private_endpoint_data_factory](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/private_endpoint) | resource |
| [azurerm_private_endpoint.private_endpoint_postgresql](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/private_endpoint) | resource |
| [azurerm_resource_group_template_deployment.data_factory](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/resource_group_template_deployment) | resource |
| [azurerm_role_assignment.data_factory_role_assignment_integration_runtime_self_hosted](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/role_assignment) | resource |
| [azurerm_user_assigned_identity.managed_identity](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/resources/user_assigned_identity) | resource |
| [random_password.random_adf_password](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/password) | resource |
| [random_password.random_postgresql_password](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/password) | resource |
| [random_password.random_psql_adf_orca_password](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/password) | resource |
| [random_password.random_psql_devops_orca_password](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/password) | resource |
| [random_password.random_psql_spotfire_activation_enrollment_password](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/password) | resource |
| [random_password.random_psql_spotfire_clin_ops_reports_password](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/password) | resource |
| [random_password.random_spotfire_password](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/password) | resource |
| [azurerm_client_config.current](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/data-sources/client_config) | data source |
| [azurerm_data_factory.this](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/data-sources/data_factory) | data source |
| [azurerm_key_vault.key_vault](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/data-sources/key_vault) | data source |
| [azurerm_log_analytics_workspace.hub](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/data-sources/log_analytics_workspace) | data source |
| [azurerm_monitor_diagnostic_categories.data_factory](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/data-sources/monitor_diagnostic_categories) | data source |
| [azurerm_monitor_diagnostic_categories.postgresql](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/data-sources/monitor_diagnostic_categories) | data source |
| [azurerm_private_dns_zone.private_dns_data_factory](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/data-sources/private_dns_zone) | data source |
| [azurerm_private_dns_zone.private_dns_key_vault](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/data-sources/private_dns_zone) | data source |
| [azurerm_private_dns_zone.private_dns_postgresql](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/data-sources/private_dns_zone) | data source |
| [azurerm_private_dns_zone.private_dns_storage_account](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/data-sources/private_dns_zone) | data source |
| [azurerm_storage_account.storage_account](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/data-sources/storage_account) | data source |
| [azurerm_subnet.subnet_sponsor](https://registry.terraform.io/providers/hashicorp/azurerm/3.23.0/docs/data-sources/subnet) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_PostgreSQL_Username"></a> [PostgreSQL\_Username](#input\_PostgreSQL\_Username) | n/a | `string` | `"dmadminuser"` | no |
| <a name="input_account"></a> [account](#input\_account) | The ADF Account Project | `string` | `""` | no |
| <a name="input_adf_name"></a> [adf\_name](#input\_adf\_name) | n/a | `string` | `""` | no |
| <a name="input_adls_name"></a> [adls\_name](#input\_adls\_name) | n/a | `string` | `""` | no |
| <a name="input_ag_name"></a> [ag\_name](#input\_ag\_name) | n/a | `string` | `""` | no |
| <a name="input_alertsemail"></a> [alertsemail](#input\_alertsemail) | The email to receive alerts | `string` | `""` | no |
| <a name="input_branch"></a> [branch](#input\_branch) | The ADF branch name | `string` | `""` | no |
| <a name="input_branch_network"></a> [branch\_network](#input\_branch\_network) | n/a | `string` | `""` | no |
| <a name="input_branch_no_network"></a> [branch\_no\_network](#input\_branch\_no\_network) | n/a | `string` | `""` | no |
| <a name="input_branch_no_network_without_dash"></a> [branch\_no\_network\_without\_dash](#input\_branch\_no\_network\_without\_dash) | n/a | `string` | `""` | no |
| <a name="input_environment"></a> [environment](#input\_environment) | The Environment name, i.e dev, staging, qa, preprod, test, prod... | `string` | `""` | no |
| <a name="input_global_env"></a> [global\_env](#input\_global\_env) | n/a | `string` | `""` | no |
| <a name="input_kv_name"></a> [kv\_name](#input\_kv\_name) | n/a | `string` | `""` | no |
| <a name="input_location"></a> [location](#input\_location) | The Location to be deployed | `string` | `""` | no |
| <a name="input_mi_name"></a> [mi\_name](#input\_mi\_name) | n/a | `string` | `""` | no |
| <a name="input_pip-version"></a> [pip-version](#input\_pip-version) | The version of execution | `string` | `""` | no |
| <a name="input_project"></a> [project](#input\_project) | The ADF Project | `string` | `""` | no |
| <a name="input_psql_name"></a> [psql\_name](#input\_psql\_name) | n/a | `string` | `""` | no |
| <a name="input_repository"></a> [repository](#input\_repository) | The ADF Repository | `string` | `""` | no |
| <a name="input_resource_group_NET"></a> [resource\_group\_NET](#input\_resource\_group\_NET) | The Resource Group name to be deployed | `string` | `""` | no |
| <a name="input_resource_group_NET_bizops"></a> [resource\_group\_NET\_bizops](#input\_resource\_group\_NET\_bizops) | n/a | `string` | `""` | no |
| <a name="input_resource_group_NET_hub"></a> [resource\_group\_NET\_hub](#input\_resource\_group\_NET\_hub) | The Resource Group name to be deployed | `string` | `""` | no |
| <a name="input_resource_group_name"></a> [resource\_group\_name](#input\_resource\_group\_name) | The Resource Group name to be deployed | `string` | `""` | no |
| <a name="input_root_folder"></a> [root\_folder](#input\_root\_folder) | The folder where locate ADF artifacts | `string` | `""` | no |
| <a name="input_service"></a> [service](#input\_service) | The name of Subscription | `string` | `""` | no |
| <a name="input_service_network"></a> [service\_network](#input\_service\_network) | n/a | `string` | `""` | no |
| <a name="input_service_network_without_dash"></a> [service\_network\_without\_dash](#input\_service\_network\_without\_dash) | n/a | `string` | `""` | no |
| <a name="input_service_no_network"></a> [service\_no\_network](#input\_service\_no\_network) | n/a | `string` | `""` | no |
| <a name="input_service_no_network_without_dash"></a> [service\_no\_network\_without\_dash](#input\_service\_no\_network\_without\_dash) | n/a | `string` | `""` | no |
| <a name="input_sponsor"></a> [sponsor](#input\_sponsor) | The name of Sponsor | `string` | `""` | no |
| <a name="input_subnet_bizops"></a> [subnet\_bizops](#input\_subnet\_bizops) | n/a | `string` | `""` | no |
| <a name="input_subnet_hub"></a> [subnet\_hub](#input\_subnet\_hub) | n/a | `string` | `""` | no |
| <a name="input_subscription_hub_id"></a> [subscription\_hub\_id](#input\_subscription\_hub\_id) | The Subscription to be deployed | `string` | `""` | no |
| <a name="input_subscription_sponsor_id"></a> [subscription\_sponsor\_id](#input\_subscription\_sponsor\_id) | The Subscription to be deployed | `string` | `""` | no |
| <a name="input_tag_business_criticality"></a> [tag\_business\_criticality](#input\_tag\_business\_criticality) | n/a | `string` | `"Low"` | no |
| <a name="input_tag_business_unit"></a> [tag\_business\_unit](#input\_tag\_business\_unit) | n/a | `string` | `"IT Operations"` | no |
| <a name="input_tag_cost_center"></a> [tag\_cost\_center](#input\_tag\_cost\_center) | n/a | `string` | `"IT-Ops"` | no |
| <a name="input_tag_data_class"></a> [tag\_data\_class](#input\_tag\_data\_class) | n/a | `string` | `"General"` | no |
| <a name="input_tag_ops_team"></a> [tag\_ops\_team](#input\_tag\_ops\_team) | n/a | `string` | `"Cloud Operations"` | no |
| <a name="input_tag_owner"></a> [tag\_owner](#input\_tag\_owner) | n/a | `string` | `"it-ops@rhoworld.com"` | no |
| <a name="input_virtual_network"></a> [virtual\_network](#input\_virtual\_network) | n/a | `string` | `""` | no |
| <a name="input_virtual_network_bizops"></a> [virtual\_network\_bizops](#input\_virtual\_network\_bizops) | n/a | `string` | `""` | no |
| <a name="input_virtual_network_hub"></a> [virtual\_network\_hub](#input\_virtual\_network\_hub) | n/a | `string` | `""` | no |

## Outputs

No outputs.
<!-- END_TF_DOCS -->
