### Proxmox on Hetzner BareMetal with ansible

I made this project just for fun, it allows you to create a proxmox host on Hetzner BareMetal

Tested on Hetzner EX43 at HEL1


feel free and send merge requests :)

#### Requirements

Server in rescue mode

#### Variables

 * `hetzner_pve_luks_pass` [default: `secret` ]: Luks encryption password 
 * `hetzner_pve_ssh_keys` [default: `secret` ]: Your SSH Pubkey to login (openssh,busybox boot)
 * `hetzner_pve_acme_mail` [default: `email@example.com` ]: Mail address for acme by letsencrypt
 * `hetzner_pve_acme_domain` [default: `vmhost.domain.com` ]: fqdn from your vmhost - must reachable from external
 * `hetzner_pve_storagebox_server` : storagebox / cifs account to automount
 * `hetzner_pve_network`  [default: `true` ]: create a vmbr1 and routes that - more info: https://github.com/extremeshok/xshok-proxmox#creates-a-routed-vmbr0-and-nat-vmbr1-network-configuration-for-proxmox-network-configuresh-run-once
 * `hetzner_pve_custom_packages`:  list of custom packages to install


#### Todos

  * Update root password
  * Hetzner API - set server into rescue mode
  * Simple monitoring via mail
  * ...
  * ...


thanks to https://github.com/extremeshok/xshok-proxmox
