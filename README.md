# Windows Server VM in Azure - Secure Web Server Project

## Overview

This project is currently **In Progress**

---

## Architecture
- Windows Server 2025 VM
- Network Security Group (NSG)
- Public IP for web access

---

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
- Screenshot: ![Remote Connection](images/vm-rdp1.png)
  ![Remote Connection](images/vm-rdp2.png)

## Troubleshooting

### Issue: RDP login failed (account locked / password issue)

While connecting to the VM via RDP, I encountered a login issue caused by an incorrect password and account lockout.

### Solution:
- Reset the password using Azure Portal
- Used Azure CLI to unlock the user account

**Result:**  
Successfully restored access to the VM and verified RDP connectivity.
