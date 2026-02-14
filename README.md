# pfSense
Default gateway for the virtual lab network, handling routing and firewall rules.

[**PT-BR**](./docs/README.pt-br.md)

## Dependencies
- [Oracle VirtualBox](https://www.virtualbox.org/) — Virtualization platform
- [pfSense CE](https://shop.netgate.com/products/netgate-installer) — Community Edition ISO

## Getting Started / Instalation / Usage
<details>
  <summary>Virtual Machine configuration</summary>

  - Base Memory: 1024 MB;
  - Number of CPUs: 1 CPU;
  - Disk Size: 8,00 GB.

  Create a new VM and attach two network adapters/Network Interface Card:
  1. **Adapter 1** — WAN (NAT or Bridged);
  2. **Adapter 2** — LAN (Internal Network - homelab).

</details>

<details>
  <summary>PfSense Configuration</summary>

  - Default username: admin
  - Default password: pfsense
  - Change the password in the User Manager;
  - IP Address: 192.168.1.1/24;
  - DHCP range: 192.168.1.100 - 192.168.1.150;
  - IPv6 disabled for network studies clarity.
  
</details>

## Roadmap
- [x] Task complete
- [ ] Task TODO

## Troubleshooting
Common issues and their solutions.

[Full Troubleshooting Guide](./docs/TROUBLESHOOTING.md)

### Error Title (error code)
- **Problem:** 
- **Solution:**