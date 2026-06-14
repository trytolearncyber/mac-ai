# 02_Skills/Current_Skills.md

> **Last Updated:** June 14, 2026

---

## 📊 Skills Overview

| Domain | Level | Topics |
|--------|-------|--------|
| **Cisco Networking** | Intermediate to Advanced | 56 |
| **Linux Administration** | Intermediate | 87 |
| **Home/Office Networking** | Advanced | 114 |
| **MikroTik** | Advanced | 60+ |
| **Fortinet Firewall** | Intermediate | 74 |
| **AWS Cloud** | Beginner to Intermediate | 75 |
| **AI / LLM** | Beginner (Learning) | In progress |

---

## 🟢 1. Cisco Networking (56 Topics)

### Layer 2 Switching

| Topic | Details |
|-------|---------|
| **VLAN** | Creation, Deletion, Access/Trunk, Native VLAN, Voice VLAN |
| **VTP** | Server/Client/Transparent modes, Pruning, Revision Number |
| **EtherChannel** | LACP, PAgP, Load Balancing, Misconfiguration Guard |
| **Inter-VLAN Routing** | SVI, Router-on-a-Stick, Subinterfaces |
| **Router on a Stick** | dot1q Encapsulation, Native VLAN |
| **Spanning Tree Protocol** | 802.1D, 802.1w, Root Bridge, Port Roles/States, PortFast, BPDUGuard |

### Layer 2 Security

| Topic | Details |
|-------|---------|
| **Port Security** | Sticky MAC, Max MAC, Violation Modes (shutdown/restrict/protect) |
| **DHCP Snooping** | Trusted/Untrusted Ports, Binding Table |
| **Dynamic ARP Inspection** | Validate ARP Against DHCP Snooping |
| **BPDU Guard** | Err-Disable on BPDU Receive |
| **Root Guard** | Prevent Downstream Root Bridge |

### Routing Technologies

| Topic | Details |
|-------|---------|
| **Routing Fundamentals** | Longest Prefix Match, AD, Metric |
| **Static Routing** | ip route, Next-hop vs Exit Interface |
| **Default Routing** | 0.0.0.0 0.0.0.0 |
| **RIP** | Version 1 vs 2, Passive Interface, Split Horizon |
| **EIGRP** | Feasible Distance, Variance, K-Values |
| **OSPF** | OSPFv2, Router ID, DR/BDR, Areas, LSA 1-5 |

### Network Services

| Topic | Details |
|-------|---------|
| **DHCP** | Server, Helper-Address, Relay |
| **DNS** | ip domain-lookup, ip name-server, ip host |
| **NTP** | ntp server, ntp master, Authentication |
| **Syslog** | logging host, Severity Levels 0-7, Source Interface |

### Remote Access & Management

| Topic | Details |
|-------|---------|
| **Telnet** | line vty, password, transport input telnet |
| **SSH** | RSA Key, transport input ssh, Version 2 |
| **HTTP/HTTPS** | ip http server, secure-server, Authentication |
| **CDP** | cdp run, show cdp neighbors |
| **LLDP** | lldp run, transmit/receive |

### Security

| Topic | Details |
|-------|---------|
| **ACL** | Standard, Extended, Named, Implicit Deny |
| **NAT** | Static NAT, Dynamic NAT, inside/outside |
| **PAT** | Overload, Single Public to Many Private |
| **ACL with NAT** | NAT Order of Operation |
| **Password Assignment** | Enable Secret, Console, Service Password-Encryption |
| **Password Recovery** | Break Sequence, Config Register 0x2142, Mode Button |

### VPN & Tunneling

| Topic | Details |
|-------|---------|
| **VPN Fundamentals** | Tunnel vs Transport, IKE Phase 1 & 2, ESP/AH |
| **GRE Tunnel** | tunnel source/destination, Tunnel Interface |
| **GRE over IPsec** | Crypto Map, Tunnel Protection |
| **Site-to-Site IPsec VPN** | ISAKMP Policy, Pre-Shared Key, Crypto Map |

### System & Maintenance

| Topic | Details |
|-------|---------|
| **IOS Upgradation** | copy tftp flash, boot system, ROMmon |
| **EVE-NG Lab Setup** | QEMU Images, Network Clouds, Wireshark |
| **Add Laptop/PC to EVE-NG** | VPCS, Static IP, DHCP Client |

### Advanced Topics

| Topic | Details |
|-------|---------|
| **HSRP** | Virtual IP/MAC, Priority, Preempt, Tracking |
| **VRRP** | Open Standard, No Preempt by Default |
| **GLBP** | Load Balancing, AVF/AVG, 4 MACs |
| **Basic BGP** | eBGP vs iBGP, neighbor, network (different meaning) |
| **Redistribution** | redistribute command, Seed Metrics, Mutual Redistribution |
| **Route Summarization** | ip summary-address, Area Range, Manual Summary |
| **Floating Static Route** | ip route with Higher AD (e.g., 200) |
| **IPv6 Basics** | GUA, LLA, Unique Local, EUI-64, NDP |
| **IPv6 Routing** | ipv6 route, OSPFv3, SLAAC, DHCPv6 |
| **SNMP** | v1/v2c (Community), v3 (Auth/Privacy), Traps |
| **NetFlow** | Flow Monitor/Record/Exporter, Input/Output |
| **QoS Basics** | Classification, Marking, Queuing, Policing/Shaping |
| **Wireless Basics** | SSID, BSS/ESS, 2.4/5GHz, WPA2, CAPWAP |
| **Network Automation Basics** | JSON/YAML/XML, Northbound/Southbound, RESTCONF/NETCONF |
| **Ansible for Cisco** | ios_command, ios_config, Inventory, Playbook |
| **REST API Basics** | GET/POST/PUT/DELETE, Status Codes, Authentication |
| **SDN Fundamentals** | Controller-Based, DNA Center, SD-WAN, OpenFlow |

---

## 🟢 2. Linux Administration (87 Topics)

### Linux Fundamentals

| Topic | Details |
|-------|---------|
| **Linux Installation** | Ubuntu/RHEL/Debian Installation, Partitioning, Bootloader |
| **Linux File System** | / (root), /home, /etc, /var, /usr, /tmp, /proc |
| **Basic Linux Concepts** | CLI basics, man pages, pipes, redirection, grep, awk, sed |
| **User Management** | useradd, usermod, userdel, passwd, /etc/passwd, /etc/shadow |
| **File Permissions** | chmod (755/644), chown, chgrp, umask, SUID, SGID, Sticky Bit |
| **Package Management** | apt (Debian/Ubuntu), yum/dnf (RHEL/CentOS), dpkg, rpm |

### Networking for Linux Servers

| Topic | Details |
|-------|---------|
| **IP Address Configuration** | ifconfig, ip addr, /etc/network/interfaces, Netplan |
| **Gateway Configuration** | route add default, ip route, /etc/network/interfaces |
| **DNS Configuration** | /etc/resolv.conf, nameserver, /etc/hosts |
| **Hostname Setup** | hostnamectl, /etc/hostname, /etc/hosts update |
| **Static IP Setup** | Netplan (Ubuntu), /etc/sysconfig/network-scripts/ (RHEL) |
| **SSH Access** | ssh client, ssh-keygen, ssh-copy-id, ~/.ssh/authorized_keys |

### Service Management

| Topic | Details |
|-------|---------|
| **systemd** | systemctl commands, unit files, targets (runlevels) |
| **Service Start/Stop/Restart** | systemctl start/stop/restart/reload |
| **Enable Auto Start Services** | systemctl enable/disable, systemctl is-enabled |

### Web Server Administration

| Topic | Details |
|-------|---------|
| **Nginx Installation** | apt install nginx, yum install nginx, verify with systemctl |
| **Nginx Virtual Host** | server block, server_name, root, index, sites-available/enabled |
| **Nginx Reverse Proxy** | proxy_pass, proxy_set_header, upstream |
| **Nginx SSL Configuration** | Let's Encrypt, certbot, SSL certificates, HTTPS redirect |
| **Apache Installation** | apt install apache2, yum install httpd |
| **Apache Virtual Host** | VirtualHost, ServerName, DocumentRoot, Directory directive |
| **Apache PHP Integration** | libapache2-mod-php, php-fpm, .php files handling |

### Database Server Administration

| Topic | Details |
|-------|---------|
| **MySQL/MariaDB Installation** | apt install mariadb-server, mysql_secure_installation |
| **Create Database** | CREATE DATABASE, SHOW DATABASES, USE database |
| **User & Permission Management** | CREATE USER, GRANT, REVOKE, FLUSH PRIVILEGES |
| **Backup & Restore** | mysqldump, mysql < backup.sql, cron automated backup |

### DNS Server Administration

| Topic | Details |
|-------|---------|
| **Bind9 Installation** | apt install bind9, named service, /etc/bind/ |
| **Zone File Configuration** | /etc/bind/named.conf.local, zone definition |
| **Forward Lookup Zone** | A records, CNAME, TXT, TTL, SOA, NS |
| **Reverse Lookup Zone** | PTR records, in-addr.arpa, ip6.arpa |

### DHCP Server Administration

| Topic | Details |
|-------|---------|
| **IP Pool Configuration** | isc-dhcp-server, subnet declaration, range |
| **Lease Management** | /var/lib/dhcp/dhcpd.leases, lease time, default/max lease |
| **Reservation Setup** | host declaration, hardware ethernet, fixed-address |

### File Server Administration

| Topic | Details |
|-------|---------|
| **Samba Installation** | apt install samba, smb.conf, smbpasswd |
| **Samba Windows Sharing** | [share] definition, workgroup, browseable, read/write |
| **NFS Installation** | apt install nfs-kernel-server, /etc/exports |
| **NFS Linux Sharing** | exportfs, showmount, mount -t nfs, /etc/fstab |

### FTP/SFTP Server Administration

| Topic | Details |
|-------|---------|
| **vsftpd Setup** | apt install vsftpd, /etc/vsftpd.conf, anonymous/local user |
| **SFTP using SSH** | internal-sftp, ChrootDirectory, Subsystem sftp |
| **User Restriction & Security** | chroot_local_user, allow_writeable_chroot, userlist |

### Mail Server Basics

| Topic | Details |
|-------|---------|
| **Postfix** | MTA, main.cf, myhostname, mydestination, relayhost |
| **Dovecot** | MDA, IMAP/POP3, dovecot.conf, 10-master.conf, 10-mail.conf |
| **SMTP Basics** | Port 25, 587 (submission), 465 (SMTPS), relay, auth |
| **IMAP Basics** | Port 143, 993 (IMAPS), folder sync, mailbox access |

### Firewall & Security

| Topic | Details |
|-------|---------|
| **UFW (Ubuntu)** | ufw enable, ufw allow/deny, ufw status, ufw app list |
| **Firewalld (RHEL/CentOS)** | firewall-cmd, zones (public, internal), permanent/runtime |
| **Open Ports** | ufw allow 22/tcp, firewall-cmd --add-port=80/tcp |
| **Block Ports** | ufw deny 23/tcp, firewall-cmd --remove-port |
| **SSH Allow Rules** | ufw allow from 192.168.1.0/24 to any port 22 |
| **NAT Basics** | iptables -t nat, MASQUERADE, PREROUTING, POSTROUTING |

### Monitoring & Logs

| Topic | Details |
|-------|---------|
| **journalctl** | View systemd logs, -u (service), -f (follow), --since, -b (boot) |
| **syslog** | /var/log/syslog, /var/log/messages, rsyslog.conf |
| **top** | Real-time process monitoring, CPU/Memory usage, load average |
| **htop** | Enhanced top, color, mouse support, tree view |

### Storage Management

| Topic | Details |
|-------|---------|
| **Disk Partitioning** | fdisk, gdisk, parted, primary/extended/logical partitions |
| **Mounting** | mount, umount, /etc/fstab, UUID, blkid, mount options |
| **LVM** | pvcreate, vgcreate, lvcreate, lvextend, resize2fs |
| **Disk Usage Analysis** | df -h, du -sh *, ncdu, iostat |

### Backup System

| Topic | Details |
|-------|---------|
| **rsync** | Local/remote sync, -avz, --delete, --exclude, ssh |
| **tar** | tar -cvf, -xvf, -zcvf (gzip), -jcvf (bzip2), incremental |
| **gzip** | Compression, gunzip, gzip -d, compression levels (1-9) |
| **Automated Backup** | cron + rsync script, crontab, log rotation |

### SSH & Remote Administration

| Topic | Details |
|-------|---------|
| **SSH Hardening** | Port change (2222), Protocol 2, MaxAuthTries, AllowUsers |
| **Key-Based Authentication** | ssh-keygen (RSA/ED25519), ~/.ssh/config, agent forwarding |
| **Disable Root Login** | PermitRootLogin no, Use sudo instead |

### Shell Scripting & Automation

| Topic | Details |
|-------|---------|
| **Bash Scripting** | #!/bin/bash, variables, loops (for/while), conditions (if/else), functions |
| **Cron Jobs** | crontab -e, * * * * * syntax, @reboot, @daily, @hourly |
| **Automation Tasks** | Backup script, log rotation, monitoring, health check |

### Virtualization

| Topic | Details |
|-------|---------|
| **KVM** | virt-manager, libvirt, qemu, bridged networking |
| **VMware** | ESXi, vSphere, VM creation, snapshots, resource allocation |
| **VirtualBox** | VMs, NAT/Host-Only/Bridged, shared folders, snapshots |

### Container Basics

| Topic | Details |
|-------|---------|
| **Docker** | docker run, ps, images, pull, build, exec, logs |
| **Docker Images** | Dockerfile, FROM, RUN, COPY, CMD, ENTRYPOINT, EXPOSE |
| **Docker Compose** | docker-compose.yml, services, networks, volumes, up/down |

### Linux Security Hardening

| Topic | Details |
|-------|---------|
| **fail2ban** | Jail config, regex patterns, ban/unban, action |
| **SELinux Basics** | getenforce, setenforce, semanage, audit2why, booleans |
| **AppArmor** | aa-status, aa-complain, aa-enforce, profiles |
| **SSH Security** | Protocol 2, key-only, PermitRootLogin no, MaxSessions |
| **Permission Hardening** | SUID removal, world-writable files, umask 027 |

### Monitoring Tools

| Topic | Details |
|-------|---------|
| **Zabbix** | Server/Agent setup, hosts, templates, triggers, graphs |
| **Nagios** | NRPE, plugins, host/service definition, alerts |

### Cloud Linux Basics

| Topic | Details |
|-------|---------|
| **AWS EC2** | Instance launch, key pairs, security groups, SSH to instance |
| **Security Groups** | Inbound/outbound rules, allow/deny ports, source IP |
| **Linux Deployment in Cloud** | User data, Cloud-Init, AMI, EBS volume attachment |

### Automation & DevOps Starter

| Topic | Details |
|-------|---------|
| **Git** | clone, add, commit, push, pull, branch, merge, .gitignore |
| **CI/CD Basics** | Jenkins, GitHub Actions, pipeline, build, test, deploy |
| **API Basics** | REST, curl, GET/POST, JSON, authentication (API key/OAuth) |

---

## 🟢 3. Home & Office Networking (114 Topics)

### Core Concepts

| Topic | Details |
|-------|---------|
| **Network Basics** | Home vs Office Network Basic Requirements |
| **Basic Network Flow** | ISP → Modem → Router → Switch/AP → Devices |
| **Core Devices** | Modem/ONT Functions (Fiber/Cable Connection) |
| **Router Functions** | Internet Sharing, WiFi, Device Management |
| **Switch Functions** | Add More LAN Ports |
| **Access Point (AP) Functions** | WiFi Coverage |
| **LAN Cable Selection** | Cat5e vs Cat6 |

### Hardware & Cabling

| Topic | Details |
|-------|---------|
| **Cable Termination** | RJ45 Crimping (T568B Standard) |
| **Cable Testing** | Cable Testing with Network Tester |
| **Cable Management** | Basic Cable Length Limits and Quality |

### SOHO Router Basics

| Topic | Details |
|-------|---------|
| **Access Methods** | Web Interface Access (192.168.0.1, 192.168.1.1) |
| **Default Credentials** | admin/admin |
| **Initial Setup** | Factory Reset Using Reset Button |
| **Quick Setup** | Quick Setup Wizard Configuration |
| **Change Password** | Change Default Admin Password |

### SOHO Router WAN

| Topic | Details |
|-------|---------|
| **PPPoE Configuration** | ISP Username/Password for DSL/Fiber |
| **Dynamic IP** | DHCP Client for Cable/FTTH |
| **Static IP** | Static IP Configuration on WAN |

### SOHO Router LAN

| Topic | Details |
|-------|---------|
| **IP Assignment** | Change LAN IP Address (Router Admin IP) |
| **DHCP Server** | Enable/Disable DHCP Server |
| **DHCP Range** | Configure DHCP Range (IP Pool for Devices) |
| **DHCP Lease Time** | Set DHCP Lease Time |
| **Address Reservation** | Static IP for Specific Devices (Printer, CCTV) |
| **DNS** | Change DNS Servers (8.8.8.8, 1.1.1.1) |

### SOHO Router Advanced

| Topic | Details |
|-------|---------|
| **Port Forwarding** | For CCTV / Gaming / Server |
| **Access Control** | Website Blocking (Block Facebook/YouTube) |
| **Device Schedule** | Internet Time for Kids/Employees |
| **Bandwidth Control** | Per Device Bandwidth Limit |
| **Parental Control** | Internet Access Time Schedule for Kids |
| **Content Filtering** | Adult, Social Media Block |

### SOHO Router Advanced Features

| Topic | Details |
|-------|---------|
| **Mesh WiFi** | Mesh Node Pairing for Whole Home Coverage |
| **QoS** | Prioritize Gaming/Streaming/Video Calls |
| **LED Control** | Disable Router LEDs (Night Mode) |
| **Reboot Schedule** | Auto Reboot Daily/Weekly for Performance |

### SOHO Router Monitoring

| Topic | Details |
|-------|---------|
| **Device Management** | View Connected Device List (Who is using WiFi) |
| **Bandwidth Usage** | Real-Time Traffic Monitoring per Device |

### SOHO Router Troubleshooting

| Topic | Details |
|-------|---------|
| **Internet Issue** | ISP Connection Status Check |
| **WiFi Issue** | WiFi Signal Strength and Interference Check |
| **Hard Reset** | 30-30-30 Hard Reset Method |

### SOHO Router Maintenance

| Topic | Details |
|-------|---------|
| **Firmware** | Check and Update Router Firmware |
| **Backup** | Backup Router Configuration |
| **Restore** | Restore Configuration from Backup |

### MikroTik Basics

| Topic | Details |
|-------|---------|
| **Access Methods** | WinBox Installation and Connection |
| **WebFig Access** | Browser Interface |
| **Factory Reset** | Reset MikroTik Router |
| **Change Password** | Change Default Admin Password |
| **Set Identity** | Set Router Identity and Clock |

### MikroTik WAN

| Topic | Details |
|-------|---------|
| **Connect ISP Modem** | Connect ISP Modem to MikroTik WAN Port |
| **DHCP Client** | Configure DHCP Client on WAN (Cable/FTTH) |
| **PPPoE Client** | Configure PPPoE Client (DSL/Fiber) |

### MikroTik LAN

| Topic | Details |
|-------|---------|
| **Bridge Setup** | Create Bridge for LAN Ports |
| **IP Assignment** | Assign IP Address to LAN Interface |
| **Set LAN Gateway** | e.g., 192.168.10.1/24 |

### MikroTik DHCP

| Topic | Details |
|-------|---------|
| **IP Pool** | Create IP Pool (DHCP Range) |
| **Server Setup** | Configure DHCP Server on LAN |
| **Set Gateway and DNS** | Gateway and DNS on DHCP Server |
| **Static DHCP Lease** | Reserved IP for Printer/CCTV |

### MikroTik DNS

| Topic | Details |
|-------|---------|
| **Set DNS Servers** | 8.8.8.8, 1.1.1.1 |
| **Allow Remote Requests** | Enable Allow Remote Requests |

### MikroTik NAT

| Topic | Details |
|-------|---------|
| **Masquerade NAT** | Configure Masquerade NAT for Internet Access |
| **Verify Internet** | Internet Connectivity from LAN Devices |
| **Port Forwarding** | Port Forwarding for CCTV/Server |

### MikroTik Bandwidth Control

| Topic | Details |
|-------|---------|
| **Why Bandwidth Control** | Bandwidth Control Importance |
| **Simple Queue** | Configure Simple Queue (Per IP Speed Limit) |
| **Upload/Download Limits** | Set Upload/Download Different Limits |
| **Burst** | Temporary Higher Speed for Browsing |
| **Per User Limit** | Per User Speed Limit for Office Employees |
| **PCQ** | Understand PCQ (Equal Sharing When Many Users Active) |
| **Simple PCQ** | PCQ for Equal Bandwidth Distribution |
| **Address List** | Group Multiple IPs for Same Limit |

### MikroTik WiFi Management

| Topic | Details |
|-------|---------|
| **Enable Wireless** | Enable Wireless Interface |
| **SSID** | Configure SSID (WiFi Name) |
| **Security Profile** | Configure Security Profile (WPA2/WPA3) |
| **WiFi Password** | Set WiFi Password |
| **2.4GHz Band** | Range, Wall Penetration for Home |
| **5GHz Band** | Speed for Office |
| **Separate SSIDs** | Separate SSIDs for 2.4GHz and 5GHz |
| **Guest Network** | Configure Guest WiFi (Separate SSID for Visitors) |
| **Client Isolation** | Guests Cannot See Each Other |
| **Guest Bandwidth Limit** | Guests Don't Slow Main Network |
| **MAC Filtering** | Allow Only Known Devices / Block Unknown |
| **Non-Overlapping Channels** | Choose 1,6,11 for Better Speed |
| **Hide SSID** | Optional - Hide WiFi Name |
| **Scan for Interference** | Scan for WiFi Interference (Find Best Channel) |
| **Check WiFi Clients** | Check WiFi Client Connections |

### MikroTik VLAN

| Topic | Details |
|-------|---------|
| **VLAN Concept** | Separate Networks for Staff/Guest |
| **VLAN 10 - Staff** | Staff Network (Internal Office) |
| **VLAN 30 - Guest** | Guest WiFi Network (Visitors) |
| **VLAN 40 - CCTV** | CCTV Network (Security Cameras) |
| **Inter-VLAN Routing** | Configure Inter-VLAN Routing |

### MikroTik Firewall

| Topic | Details |
|-------|---------|
| **Block Guest Network** | Block Guest from Accessing Office Internal Network |
| **Allow Guest Internet** | Allow Guest Network to Access Internet Only |
| **Block WinBox from WAN** | Block WinBox Access from WAN (Security) |
| **Allow WinBox from LAN** | Allow WinBox Access from LAN Only |
| **Block Ping from WAN** | Hide Router from Internet |

### MikroTik Security

| Topic | Details |
|-------|---------|
| **Change Password** | Change Default MikroTik Password |
| **Disable Unused Ports** | Ethernet Ports Not in Use |
| **Disable Unused Services** | FTP, Telnet, API if not needed |
| **Enable HTTPS** | HTTPS for Web Access |
| **Update Firmware** | Update RouterOS Firmware (Security Patches) |
| **Regular Backup** | Regular Configuration Backup |
| **Export to Script** | Export Configuration to Script File |
| **Disable WPS** | WiFi Protected Setup - Security Risk |

### IP Planning

| Topic | Details |
|-------|---------|
| **Home IP Scheme** | Simple IP Scheme for Home (192.168.1.0/24) |
| **Office IP Scheme** | Simple IP Scheme for Office (192.168.10.0/24) |
| **Static IP Assignment** | Assign Static IPs for Server, Printer, CCTV |
| **Documentation** | Write Down IP Addresses (Simple Excel List) |

### Monitoring & Troubleshooting

| Topic | Details |
|-------|---------|
| **Internet Check** | Check if Internet is Working (Ping 8.8.8.8) |
| **Connected Devices** | Check Who is Using WiFi |
| **WiFi Signal** | Check WiFi Signal Strength |
| **Restart Router** | Restart Router When Internet Slow |

### Backup & Maintenance

| Topic | Details |
|-------|---------|
| **Backup Config** | Backup Router Configuration Before Any Change |
| **Restore Config** | Restore Configuration if Something Breaks |
| **Factory Reset** | Factory Reset When Completely Stuck |

---

## 🟢 4. Fortinet Firewall (74 Topics)

### Introduction & Installation

| Topic | Details |
|-------|---------|
| **FortiGate Basics** | Full Configuration Basics |
| **FortiGate Setup** | Setup for Beginners |
| **EVE-NG Installation** | Install FortiGate on EVE-NG |
| **GNS3 Installation** | Install FortiGate on GNS3 |
| **VMware Installation** | Install FortiGate on VMware |
| **AWS Installation** | Install FortiGate on AWS EC2 |

### Lab Setup & Emulator

| Topic | Details |
|-------|---------|
| **GNS3 Lab** | GNS3 Lab Setup for FortiGate |
| **VMware Lab** | VMware Configuration for FortiGate Lab |
| **Cloud Integration** | Cloud Setup Integration (GNS3 + Internet) |
| **Cisco Integration** | Cisco IOU L2/L3 Integration in GNS3 |

### Basic Network Configuration

| Topic | Details |
|-------|---------|
| **LAN/WAN** | LAN & WAN Configuration |
| **IP Addressing** | IP Address Configuration |
| **Interface** | Interface Configuration |
| **Gateway** | Gateway Setup |

### VLAN & Switching Integration

| Topic | Details |
|-------|---------|
| **VLAN Configuration** | VLAN Configuration in FortiGate |
| **Sub-Interfaces** | VLAN Sub-Interfaces Setup |
| **Inter-VLAN Routing** | Inter-VLAN Routing |
| **Cisco Integration** | Cisco Switch Integration with FortiGate |

### NAT Configuration

| Topic | Details |
|-------|---------|
| **NAT Setup** | NAT Setup in FortiGate |
| **Source NAT (SNAT)** | Source NAT Configuration |
| **Destination NAT (DNAT)** | Destination NAT / Virtual IP |
| **Port Forwarding** | Port Forwarding Configuration |

### Security & Policies

| Topic | Details |
|-------|---------|
| **Firewall Policies** | Firewall Policy Configuration |
| **Access Rules** | Access Rules Setup |
| **Traffic Control** | Traffic Control Basics |

### VPN Configuration

| Topic | Details |
|-------|---------|
| **IPsec VPN** | IPsec VPN (Site-to-Site) |
| **Remote Access VPN** | Remote Access VPN (IPsec / SSL VPN) |
| **Cross-Platform VPN** | VPN between FortiGate and Checkpoint |
| **VPN Troubleshooting** | VPN Troubleshooting |

### Advanced Networking

| Topic | Details |
|-------|---------|
| **Link Aggregation** | Link Aggregation (LACP) |
| **SD-WAN** | SD-WAN Configuration |
| **GRE Tunnel** | GRE Tunnel Configuration |
| **Link Monitoring** | Link Monitoring |

### High Availability & Management

| Topic | Details |
|-------|---------|
| **HA Setup** | HA (High Availability) Setup |
| **FortiManager** | FortiManager Installation |
| **FortiManager Integration** | Add FortiGate to FortiManager |
| **ADOM** | ADOM Configuration in FortiManager |

### DMZ & Network Segmentation

| Topic | Details |
|-------|---------|
| **DMZ Setup** | DMZ (Demilitarized Zone) Setup |
| **Perimeter Network** | Perimeter Network Design |
| **Security Zones** | Security Zone Configuration |

### Troubleshooting & Debugging

| Topic | Details |
|-------|---------|
| **CLI Troubleshooting** | FortiGate CLI Troubleshooting |
| **Advanced Debugging** | Advanced Debugging Commands |
| **VPN Debug** | VPN Troubleshooting |
| **Network Diagnosis** | Network Issue Diagnosis |

### Automation & Backup

| Topic | Details |
|-------|---------|
| **Config Backup** | Configuration Backup to FTP Server |
| **Automated Script** | Automated Backup Script for FortiGate |
| **Python Script** | Python Script for Firewall Backup |

### Cloud Integration

| Topic | Details |
|-------|---------|
| **AWS Deployment** | FortiGate Deployment in AWS Cloud |
| **Cloud Firewall** | Cloud Firewall Setup Basics |

### Endpoint Security

| Topic | Details |
|-------|---------|
| **FortiClient** | FortiClient SSL VPN Setup (Linux Ubuntu) |

### Performance & Monitoring

| Topic | Details |
|-------|---------|
| **Traffic Monitoring** | Traffic Monitoring |
| **System Diagnostics** | System Diagnostics |

### Quick Commands

| Command | Purpose |
|---------|---------|
| show system status | System Status |
| show interface configuration | Interface Config |
| show firewall policies | Firewall Policies |
| show routing table | Routing Table |
| show active sessions | Active Sessions |
| debug flow | Debug Packet Flow |
| VPN tunnel list | VPN Tunnel |
| ike debug | IKE Debug |
| packet sniffer | Packet Sniffer |
| backup configuration | Backup Config |
| factory reset | Factory Reset |
| reboot | Reboot FortiGate |

### GUI Paths

| Path | Purpose |
|------|---------|
| Network → Network Interfaces | Interface Config |
| Network → Static Routes | Static Routes |
| Network → VLANs | VLAN Config |
| Policy → Firewall Policies | Firewall Rules |
| Policy → NAT (Virtual IP) | NAT Config |
| VPN → IPsec VPN | IPsec Config |
| VPN → SSL VPN | SSL VPN Config |
| Network → SD-WAN | SD-WAN Config |
| System → High Availability | HA Config |
| System → Configuration Backup | Backup |

---

## 🟢 5. AWS Cloud (75 Topics)

### AWS Fundamentals

| Topic | Details |
|-------|---------|
| **Global Infrastructure** | AWS Global Infrastructure Overview |
| **Region & AZ** | Region & Availability Zone Concepts |
| **Management Console** | Console Access and Navigation |
| **Free Tier Account** | AWS Free Tier Account Setup |

### IAM (Identity & Access Management)

| Topic | Details |
|-------|---------|
| **IAM Users** | IAM User Creation and Management |
| **IAM Groups** | IAM Group Creation and Management |
| **IAM Policies** | IAM Policy Creation and Attachment |
| **MFA** | Multi-Factor Authentication Configuration |
| **Root vs IAM User** | Root User vs IAM User Best Practices |
| **Access** | IAM User Login Link and Credentials |

### Compute Services

| Topic | Details |
|-------|---------|
| **EC2 Launch** | EC2 Instance Launch & Management |
| **Instance Types** | t2.micro, t3.micro Selection |
| **Instance Lifecycle** | Start, Stop, Reboot, Terminate |
| **Security Groups** | Security Group Configuration for EC2 |
| **Allow Ports** | SSH (22), HTTP (80), HTTPS (443) |
| **Key Pair** | Key Pair Generation and Management |
| **.pem File** | .pem File Usage for SSH Login |
| **Elastic IP** | Elastic IP Configuration and Association |
| **EC2 Monitoring** | CPU, Network, Disk Monitoring |

### Storage Services

| Topic | Details |
|-------|---------|
| **S3 Bucket** | S3 Bucket Creation & Management |
| **File Upload/Download** | Upload and Download to S3 |
| **Bucket Permission** | Bucket Permission Control (Public/Private) |
| **S3 Static Website** | S3 Static Website Hosting Configuration |
| **Bucket Policy** | S3 Bucket Policy Configuration |
| **EBS Volume** | EBS Volume Basics (Root, Additional) |
| **EBS Attach/Detach** | EBS Volume Attach and Detach to EC2 |

### Networking Basics

| Topic | Details |
|-------|---------|
| **VPC** | VPC Basics and Default VPC |
| **Custom VPC** | Custom VPC Creation |
| **Subnet** | Subnet Configuration (Public vs Private) |
| **CIDR Block** | CIDR Block and IP Range Selection |
| **Internet Gateway** | IGW Creation and Attachment |
| **Route Table** | Route Table Configuration for Internet Access |
| **Route Association** | Route Table Association with Subnet |
| **Public vs Private** | Public Subnet vs Private Subnet Concepts |
| **NAT** | Basic NAT Understanding for Private Subnet |

### Security Basics

| Topic | Details |
|-------|---------|
| **Security Groups** | Inbound and Outbound Rules |
| **Stateful vs Stateless** | Security Group Stateful |
| **NACL** | NACL (Network ACL) Basics |
| **NACL Rules** | NACL Stateless Rules Configuration |
| **Firewall Concepts** | Basic Firewall Concepts in AWS |
| **SG vs NACL** | Security Groups vs NACL Differences |

### Monitoring & Management

| Topic | Details |
|-------|---------|
| **CloudWatch** | CloudWatch Basics Overview |
| **Resource Monitoring** | Basic Resource Monitoring (CPU, Memory, Disk) |
| **CloudWatch Alarms** | CloudWatch Alarms Configuration |
| **Billing Dashboard** | Billing Dashboard Monitoring and Alerts |
| **Free Tier Tracking** | AWS Free Tier Usage Tracking |

### Database Basics

| Topic | Details |
|-------|---------|
| **RDS** | RDS Basics and Database Engines |
| **MySQL Deployment** | MySQL Database Deployment on AWS RDS |
| **RDS Security Group** | RDS Security Group Configuration |
| **DB Connection** | Database Connection from EC2 to RDS |

### Linux on AWS

| Topic | Details |
|-------|---------|
| **EC2 Access** | SSH Access to EC2 from Windows/Linux/Mac |
| **.pem Key SSH** | Using .pem Key for SSH Login |
| **Linux Deployment** | Linux Server Deployment on AWS EC2 |
| **Server Configuration** | Basic Server Configuration (Hostname, Timezone) |
| **Package Installation** | Installing Software on EC2 (apt, yum) |

### Deployment & Hosting

| Topic | Details |
|-------|---------|
| **EC2 Hosting** | Website Hosting on EC2 (Apache/Nginx) |
| **App Deployment** | Basic Application Deployment on EC2 |
| **Domain & DNS** | Domain & DNS Basics with Route 53 |
| **DNS Records** | Route 53 DNS Record Types (A, CNAME, MX) |
| **Point Domain** | Point Domain to EC2 Elastic IP using Route 53 |

### Backup & Recovery

| Topic | Details |
|-------|---------|
| **EBS Snapshot** | EBS Snapshot Creation and Management |
| **Snapshot Restore** | Snapshot Restore to New Volume |
| **AMI** | AMI (Amazon Machine Image) Creation Basics |
| **Custom AMI** | Launch EC2 Instance from Custom AMI |

### Automation Basics

| Topic | Details |
|-------|---------|
| **AWS CLI** | Basic AWS CLI Installation and Configuration |
| **EC2 CLI Commands** | aws ec2 describe-instances |
| **S3 CLI Commands** | aws s3 ls, cp, sync |
| **Automation Concepts** | Simple Automation Concepts (Scripting with AWS CLI) |

### Core AWS Skill Stack

| Service | Purpose |
|---------|---------|
| **EC2** | Elastic Compute Cloud |
| **S3** | Simple Storage Service |
| **IAM** | Identity and Access Management |
| **VPC** | Virtual Private Cloud |
| **Security Groups** | Firewall Rules |
| **Route 53** | DNS Management |
| **CloudWatch** | Monitoring |

---

## 📊 Skills Summary

| Domain | Level | Topics |
|--------|-------|--------|
| Cisco Networking | Intermediate to Advanced | 56 |
| Linux Administration | Intermediate | 87 |
| Home/Office Networking | Advanced | 114 |
| MikroTik | Advanced | 60+ |
| Fortinet Firewall | Intermediate | 74 |
| AWS Cloud | Beginner to Intermediate | 75 |
| **Total** | | **466+** |

---

## 🚀 What's Next (AI Automation Journey)

| Skill to Learn | Why |
|----------------|-----|
| **n8n** | Workflow automation |
| **Claude API** | AI integration |
| **Langflow** | Visual AI workflows |
| **RAG** | Document Q&A |
| **Multi-Agent Systems** | Complex automation |
| **Voice AI** | ElevenLabs, Twilio |
| **Network + AI Integration** | Combine existing skills with AI |

---

**🔖 Tags:** `#CurrentSkills` `#Cisco` `#Linux` `#MikroTik` `#Fortinet` `#AWS` `#HomeOffice` `#MACMatrix`
