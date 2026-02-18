# pfSense
Default gateway for the virtual lab network, handling routing and firewall rules.

[**PT-BR**](./docs/README.pt-br.md)

![pfSense_Dashboard](./docs/pfSense_dashboard.png)

## Dependencies
- [Oracle VirtualBox](https://www.virtualbox.org/) — Virtualization platform;
- [pfSense CE](https://shop.netgate.com/products/netgate-installer) — Netgate Installer ISO.

## Getting Started
<details>
  <summary>Virtual Machine configuration</summary>

  - Base Memory: 1024 MB;
  - Number of CPUs: 1 CPU;
  - Disk Size: 8 GB.

  Create a new VM and attach two Network Interface Cards (NICs):
  1. **Adapter 1** — WAN (NAT or Bridged);
  2. **Adapter 2** — LAN (Internal Network - homelab).

</details>

<details>
  <summary>pfSense Configuration</summary>

  1. Default username: admin
  2. Default password: pfsense

  - Change the password in the User Manager;
  - IP Address: 192.168.1.1/24;
  - DHCP range: 192.168.1.100 - 192.168.1.199;
  - IPv6 disabled to avoid noise in packet analysis.
  
</details>

## Usage
<details>
  <summary>Managing Network</summary>

  You can toggle the network connection by checking or unchecking `[ ] Virtual Cable Connection` in the pfSense VM network settings (Adapter 1 - WAN).

  - **Internet access:**
  Enable the cable connection on Adapter 1. pfSense will route traffic from the internal network through your host machine.

  - **Isolated environment:**
  Disable the cable connection on Adapter 1. The internal network remains active, but without external access — recommended for safe malware analysis or controlled testing.
</details>

<details>
  <summary>Updating pfSense</summary>

  1. **Backup current config:** Diagnostics → Backup & Restore → Download configuration as XML
  2. **Remove installed packages:** System → Package Manager → Installed Packages
  3. **Update the system:** System → Update → Confirm
  4. **If something goes wrong, restore the backup at** Diagnostics → Backup & Restore
</details>