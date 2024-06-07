<!-- BEGIN_ANSIBLE_DOCS -->

# Ansible Role: trippsc2.configure_standalone_win_dns
This role configures DNS on a standalone (non-domain) Windows machine to use the domain controller for DNS and registers its IP address in DNS.

## Requirements

| Platform | Versions |
| -------- | -------- |
| Windows | 2019, 2022 |

## Dependencies

| Collection |
| ---------- |
| community.windows |

## Role Arguments
|Option|Description|Type|Required|Choices|Default|
|---|---|---|---|---|---|
| dc_inventory_name | The Ansible inventory name of the test domain controller. | str | no |  | dc |
| dc_ip_address | The IP address of the test domain controller. | str | no |  | {{ hostvars[dc_inventory_name].ansible_host }} |
| domain_name | The name of the domain to join. | str | no |  | test.loc |
| dns_host_name | The hostname of the DNS server. | str | no |  | {{ inventory_hostname }} |
| dns_ip_address | The IP address of the DNS server. | str | no |  | {{ ansible_host }} |


## License
MIT

## Author and Project Information
Jim Tarpley
<!-- END_ANSIBLE_DOCS -->
