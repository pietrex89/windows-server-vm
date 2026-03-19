# Windows Server VM in Azure - Secure Web Server Project

## Overview

This project is currently **In Progress**

## Architecture
- Windows Server 2025 VM
- Network Security Group (NSG)
- Public IP for web access

## Steps

### 1. Virtual Machine Creation
- Created Windows Server 2025 VM in Azure
- Configured basic settings (region, size, credentials)
- **Purpose:** To deploy a functional server accessible from the internet
- Screenshot: ![VM Creation](images/vm-creation.png)

### 2. Network Security Configuration (NSG)
- RDP (port 3389) restricted to my IP only
- HTTP (port 80) allowed publicly
- Other traffic blocked
- **Purpose:** To secure remote access while allowing public web traffic
- Screenshot: ![Configure NSG](images/nsg.png)

### 3. Remote Connection (RDP)
- Connected to the VM using Remote Desktop Protocol
- Verified successful login and access to Windows Server
- **Purpose** To manage and configure the server remotely.
- Screenshots: ![Remote Connection](images/vm-rdp1png.png)
  ![Remote Connection](images/vm-rdp2.png)

### 4. IIS Installation
- Opened Server Manager
- Installed Web Server (IIS) role
- Verified default IIS page using localhost
- **Purpose** To configure the VM as a web server.
- Screenshots: ![IIS Installation](images/iis.png)
![IIS Installation](images/iis-installation.png)
![IIS Installation](images/iis-welcome.png)

## Troubleshooting

### Issue: RDP login failed (account locked / password issue)

While connecting to the VM via RDP, I encountered a login issue caused by an incorrect password and account lockout.

### Solution:
- Reset the password using Azure Portal
- Used Azure CLI to unlock the user account

### Result:
Successfully restored access to the VM and verified RDP connectivity.
