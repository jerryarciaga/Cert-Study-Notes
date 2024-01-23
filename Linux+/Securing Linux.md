# Back to [Table of Contents](/README.md)
# Linux Hardening
* Reduce the attack surface
* Manual (editing config files) or automated - via a centralized configuration management tool such as Ansible or Puppet
* **Hardware** - apply firmware updates
* **Software** - apply kernel, OS and software package updates (`sudo apt get update; sudo apt-get upgrade`)
* Complex passwords, disallow root ssh login, disable unused components such as Apache2 web server
* Prevent direct public access (VPN, jump box, SSH tunnelling)
* Enable log forwarding, continuous monitoring
* Enable Encryption
	* Network: HTTPS, VPN, SSH tunneling, IPsec
	* Storage: dm-crypt, LUKS, third party tools
* Firewalls
	* Host-based firewall
	* Host intrusion detection/prevention system

# Managing UEFI (Unified Extensible Firmware Interface)
* Supersedes Basic Input/Output System (BIOS) since 2010
* Supports larger disks, GUI management, secure boot