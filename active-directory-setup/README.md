# Active Directory Lab — Windows Server 2022

## Overview

This project demonstrates the deployment and configuration of a Windows Server 2022 Active Directory environment using VirtualBox. The lab simulates a small enterprise infrastructure environment with integrated Active Directory, DNS, DHCP, and Windows client domain management.

The environment was built to strengthen practical skills in:
- Windows Server Administration
- Active Directory Domain Services (AD DS)
- DNS & DHCP Configuration
- Enterprise Network Infrastructure
- Identity & Access Management
- Virtualization Technologies

---

# Lab Environment

## Technologies Used

- Windows Server 2022
- Windows 10 Client
- VirtualBox
- Active Directory Domain Services (AD DS)
- DNS
- DHCP

---

# Objectives

- Configure a Windows Server 2022 Domain Controller
- Install and configure Active Directory Domain Services
- Configure DNS Services
- Configure DHCP Services
- Create and manage a domain environment
- Configure reverse lookup zones and PTR records
- Join a Windows 10 client machine to the domain
- Simulate a small enterprise network infrastructure

---

# Domain Information

| Configuration | Value |
|---|---|
| Domain Name | shaunmonwabisiteka.com |
| Server Role | Domain Controller |
| Client Machine | Windows10-VM00 |
| Virtualization Platform | VirtualBox |

---

# Lab Configuration Process

## 1. Server Installation & Initial Configuration

Performed the initial configuration of Windows Server 2022, including:
- Network connectivity
- Server hostname configuration
- Timezone configuration
- Server preparation for Active Directory deployment

### Server installed

![Server Configuration](./screenshots/01-server-installed.png)

---

## 2. Active Directory & DNS Installation

Installed:
- Active Directory Domain Services (AD DS)
- DNS Server

### Active Driectory & DNS installation

![AD & DNS Installation](./screenshots/02-ad-dns-installation.png)

### Active Driectory & DNS successfully installed

![AD & DNS Installation Success](./screenshots/03-ad-dns-installed-successfully.png)

---

## 3. Active Directory Domain Controller Promotion

Promoted the Windows Server to a Domain Controller and configured a new forest for the enterprise environment.

### Promoting Server

![Promoting Server](./screenshots/04-promoting-server.png)

### Active Directory Promotion Options

![AD Promotion Options](./screenshots/05-ad-promotion-options.png)

### Active Directory Promotion Succeeded

![AD Promotion Success](./screenshots/06-ad-promotion-succeeded.png)

---

## 4. Domain Creation

Successfully created the:
shaunmonwabisiteka.com domain.

### Domain created

![Domain Created](./screenshots/07-domain-created.png)

### Adding A New Forest

![Adding New Forest](./screenshots/08-adding-new-forest.png)

---

# DHCP Configuration

Installed and configured DHCP services for automatic IP address assignment within the enterprise environment.

### DHCP Configuration Included

- DHCP Role Installation
- DHCP Post-Installation Configuration
- IPv4 Scope Configuration
- DHCP Scope Range Configuration
- DHCP Security Groups
- DHCP Activation

### DHCP Installation

![DHCP Installation](./screenshots/09-dhcp-installation.png)

### DHCP Post Installation

![DHCP Post Installation](./screenshots/10-dhcp-post-installation.png)

### DHCP Console

![DHCP Console](./screenshots/11-dhcp-console.png)

### DHCP Scope

![DHCP Scope](./screenshots/12-dhcp-scope.png)

---

## IP Address Scope Configuration

Configured the DHCP IPv4 scope for automatic client IP address assignment.

### Scope Details

| Configuration | Value |
|---|---|
| Start IP Address | 192.168.1.100 |
| End IP Address | 192.168.1.254 |

### IP Address Range

![IP Address Range](./screenshots/13-ip-address-range.png)

### DHCP Active

![DHCP Active](./screenshots/14-dhcp-active.png)

---

# DNS Configuration

Configured DNS services including:
- Forward Lookup Zones
- Reverse Lookup Zones
- PTR Records

### Reverse Lookup Zone

![Reverse Lookup Zone](./screenshots/15-reverse-lookup-zone.png)

### Active Directory Users & Computers

![PTR Record Configuration](./screenshots/16-ad-users-computers.png)

### DNS Tools

![DNS Management Tools](./screenshots/17-dns-tools.png)

---

# Active Directory Administrative Tools

Used the following administrative tools:
- Active Directory Users & Computers
- DNS Management Console
- DHCP Management Console

### PTR Record

![AD Users & Computers](./screenshots/18-ptr-record.png)

---

# Domain Join Configuration

Successfully joined the Windows 10 client machine (Windows10-VM00) to the:
shaunmonwabisiteka.com domain.

### Domain Join

![Windows 10 Domain Join](./screenshots/19-domain-join.png)

---

### Domain Join Credentials

![Image 20](screenshots/20-domain-join-credentials.png)

Entered domain administrator credentials to authorize the Windows 10 client machine to join the Active Directory domain.

This step validates that only authorized administrators can add devices to the domain environment.

---

### Domain Joined Successfully

![Image 21](screenshots/21-domain-joined-successful.png)

The Windows 10 client machine was successfully joined to the Active Directory domain.

This confirms secure communication between the client workstation and the domain controller, enabling centralized identity and access management.

---

### Restart Required

![Image 22](screenshots/22-restart-to-apply-changes.png)

Windows prompted for a system restart to apply the domain membership changes.

A restart is required to complete the domain join process and update the machine's authentication relationship with the domain controller.

---

### Domain User Sign-In

![Image 23](screenshots/23-windows10-sign-in.png)

Successfully signed in to the Windows 10 client machine using Active Directory domain credentials.

This confirms that domain authentication is functioning correctly and that users can access organizational resources using centralized Active Directory accounts.

---

## Outcome

✅ Successfully joined a Windows 10 client machine to the Active Directory domain.

✅ Verified domain authentication using Active Directory user credentials.

✅ Demonstrated centralized identity and access management through Active Directory.

✅ Validated communication between the client workstation and domain controller.

---

# Skills Demonstrated

- Windows Server 2022 Administration
- Active Directory Configuration
- DNS Administration
- DHCP Administration
- Network Infrastructure Management
- Domain Controller Deployment
- Identity & Access Management
- Enterprise Environment Simulation
- Virtualization using VirtualBox

---

# Lessons Learned

This lab strengthened my practical understanding of:
- Enterprise infrastructure deployment
- Active Directory architecture
- DNS & DHCP integration
- Domain management
- Client-server communication
- Windows Server administration
- Network service configuration
- Virtualized enterprise environments

---


