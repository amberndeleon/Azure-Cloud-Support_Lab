# Azure-Cloud-Support_Lab

## Overview
This project simulates an IT support environment using Microsoft Azure, Windows Server 2022, Active Directory, Azure monitoring tools, and an  osTicket help desk system.

## Technologies Used
- Microsoft Azure
- Windows Server 2022
- Active Directory Domain Services
- Azure Monitoring
- osTicket
- Remote Desktop Protocol (RDP)

## Skills Demonstrated
- User account management
- Password resets
- Active Directory administration
- Cloud VM deployment
- Monitoring and alerts
- Help Desk Ticketing
- Remote support troubleshooting

## Project Tasks
- Created Azure VM
- Configured Active Directory
- Created employee users and groups
- Installed osTicket help desk system
- Configured Azure monitoring alerts
- Documented troubleshooting workflows

# Part 1 - Azure VM Setup

## Step 1: Create Resource Group
- Open Azure Portal
- Navigate to Resource Groups
- Create new resource group name:
  CloudSupportLab

## Step 2: Create Virtual Machine
- Open Virtual Machines
- Click Create -> Azure Virtual Machine

### VM Configuration
- VM Name: HelpDeskServer
- Region: Central US
- Image: Windows Server 2022 Datacenter
- Size: B2s
- Username: cloudadmin

### Networking 
- Enabled RDP Port 3389

## Step 3: Deploy VM
- Reviewed settings
- Created VM
- Waited for deployment completion

---

# Part 2 - Remote Desktop Connection

## MacBook Connection 
Used Bastion on macOS under "Connect" tab on the HelpDeskServer VM to remotely connect to Azure VM.

--- 

# Part 3 - Active Directory Setup

## Installed Active Directory Domain Services
- Opened Server Manager
- Add AD DS role
- Promoted server to Domain Controller

### Domain Information
- Domain Name: cloudlab.local

--- 

# Part 4 - User Management

## Created Organizational Units
- Employees
- IT
- HR
- Managers

## Created Users
- John Smith
- Emily Cruz
- Sarah Gomez
- Mike Davis
- HelpDeskAdmin

## Practiced Support Tickets
- Password resets

---
# Part 5 - Monitoring and Alerts

## Azure Monitoring
- Enabled VM Insights
- Monitored CPU and memory usage
- Configured alert rules

---
