# Active Directory Lab — Windows Server 2022

## Overview

This project demonstrates the deployment and configuration of a Windows Server 2022 Active Directory environment using VirtualBox.

The lab was designed to simulate a small enterprise infrastructure environment including:

* Active Directory Domain Services (AD DS)
* DNS Configuration
* DHCP Configuration
* Domain Controller Promotion
* Reverse Lookup Zones
* Domain Joining
* User & Computer Management

---

# Lab Environment

## Technologies Used

* Windows Server 2022
* Windows 10 Client
* VirtualBox
* Active Directory Domain Services (AD DS)
* DNS
* DHCP

---

# Objectives

* Configure a Domain Controller
* Install and configure Active Directory
* Configure DNS Services
* Configure DHCP Services
* Create and manage domains
* Configure reverse lookup zones
* Join a client machine to the domain
* Simulate an enterprise network environment

---

# Domain Information

| Configuration           | Value                  |
| ----------------------- | ---------------------- |
| Domain Name             | shaunmonwabisiteka.com |
| Server Role             | Domain Controller      |
| Client Machine          | Windows10-VM00         |
| Virtualization Platform | VirtualBox             |

---

# Lab Configuration Process

## 1. Server Installation & Initial Configuration

Configured:

* Windows Server 2022
* Network connectivity
* Server hostname
* Timezone settings

### Screenshot

![Server Configuration](screenshots/01-server-installed.png)

---

## 2. Active Directory & DNS Installation

Installed:

* Active Directory Domain Services
* DNS Server

### Screenshot

![AD Installation](screenshots/02-ad-dns-installation.png)

---

## 3. Active Directory Promotion

Promoted the server to a Domain Controller and created a new forest.

### Screenshot

![Server Promotion](screenshots/04-promoting-server.png)

### Screenshot

![Promotion Success](screenshots/06-ad-promotion-succeeded.png)

---

## 4. Domain Creation

Successfully created the domain:
shaunmonwabisiteka.com

### Screenshot

![Domain Created](screenshots/07-domain-created.png)

---

# DNS Configuration

Configured:

* Forward Lookup Zones
* Reverse Lookup Zones
* PTR Records

### Screenshot

![DNS Tools](screenshots/17-dns-tools.png)

### Screenshot

![PTR Record](screenshots/15-ptr-record.png)

---

# DHCP Configuration

Configured DHCP services for automatic IP address assignment.

### Configuration Included:

* IPv4 Scope Configuration
* DHCP Scope Range
* DHCP Security Groups
* DHCP Activation

### Scope Details

| Configuration | Value         |
| ------------- | ------------- |
| Start IP      | 192.168.1.100 |
| End IP        | 192.168.1.254 |

### Screenshot

![DHCP Console](screenshots/11-dhcp-console.png)

### Screenshot

![DHCP Scope](screenshots/12-dhcp-scope.png)

---

# Active Directory Tools

Used:

* Active Directory Users & Computers
* DNS Management Console
* DHCP Console

### Screenshot

![AD Users & Computers](screenshots/16-ad-users-computers.png)

---

# Domain Join

Successfully joined the Windows 10 client machine to the:
shaunmonwabisiteka.com domain.

### Screenshot

![Domain Join](screenshots/18-domain-join.png)

---

# Skills Demonstrated

* Windows Server Administration
* Active Directory Configuration
* DNS Administration
* DHCP Administration
* Network Infrastructure
* Virtualization
* Enterprise Environment Setup
* Identity & Access Management

---

# Lessons Learned

This lab strengthened my understanding of:

* Enterprise infrastructure deployment
* Active Directory architecture
* Domain services
* DNS & DHCP integration
* Client-server communication
* Windows Server administration

---

# Future Improvements

* Group Policy Configuration
* Organizational Units (OUs)
* User & Group Management
* Security Hardening
* SIEM Integration
* Windows Event Monitoring
