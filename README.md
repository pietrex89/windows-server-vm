# Windows Server VM in Azure - Secure Web Server Project

## Overview

This project is currently **In Progress**

## Architecture
- Windows Server 2025 VM
- Network Security Group (NSG)
- Public IP for web access

## Steps

### 1. Virtual Machine Creation:
- Created Windows Server 2025 VM in Azure
- Enabled public IP to allow web access
- **Purpose:** To deploy a functional server accessible from the internet
- Screenshot: ![VM Creation](images/vm-creation.png)

### 2. Network Security Configuration:
- RDP (port 3389) restricted to my IP only
- HTTP (port 80) allowed publicly
- Other traffic blocked
- **Purpose:** Ensures secure access and limits exposure to threats
- Screenshot: ![Configure NSG](images/nsg.png)

## Troubleshooting

### Issue: RDP login failed (account locked / password issue)

While connecting to the VM via RDP, I encountered a login issue caused by an incorrect password and account lockout.

### Solution:
- Reset the password using Azure Portal
- Used Azure CLI to unlock the user account

**Result:**  
Successfully restored access to the VM and verified RDP connectivity.
