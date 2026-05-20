# Azure-Cloud-Support_Lab

## Overview
This project simulates a small enterprise cloud support environment hosted in Microsoft Azure. The lab was designed to demonstrate foundational IT support, system administration, identity management, monitoring, and troubleshooting skills using enterprise technologies commonly found in production enviroments.

The environment includes:
- Azure virtual infrastructure
- Windows Server 2022
- Active Directory Domain Services (AD DS)
- osTicket help desk platform
- Azure monitoring and alerting
- Remote administration workflows

  The project focuses on user lifecycle management, support ticket handling, system monitoring, and troubleshooting procedures.
  
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

## Architecture

Then environment consists of: 
- 1 Windows Server 2022 VM hosted in Azure
- Active Directory Domain Services
- osTicket help desk platform
- Azure monitoring and alerting tools
- Remote administration access using Bastion and RDP

### Network Flow
User --> Azure Bastion --> HelpDeskServer VM --> Active Directory --> osTicket 

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

## macOS Remote Access 
Used Azure Bastion from macOS through the Azure portal under the Connect tab on the HelpDeskServer VM to securely remotely connect to the Azure virtual machine. 

--- 

# Part 3 - Active Directory Setup

## Installed Active Directory Domain Services
- Opened Server Manager
- Add AD DS role
- Promoted server to Domain Controller

### Domain Information
- Domain Name: cloudlab.local

--- 

# Part 4 - User and Group Management

## Created Organizational Units (OUs)

Created Organizational Units to simulate departmental separation within an enterprise environment:

- Employees
- IT
- HR
- Managers

---

## User Account Management

Created and managed user accounts to practice:
- User onboarding
- Password resets
- Group assignments
- Account lockout resolution
- Administrative privilege delegation
  
  ### Sample Users
  
- John Smith
- Emily Cruz
- Sarah Gomez
- Mike Davis
- HelpDeskAdmin

## Practiced Support Tickets
- Password resets

---
# Part 5 - Help Desk Ticketing

## osTicket Configuration

Installed and configured osTicket to simulate a real-world IT help desk environment.

### Ticket Workflow Practice

Practiced:
- Password reset tickets
- User login support
- Account unlock requests
- Basic troubleshooting workflows
- Ticket documentation and resolution

---

# Part 6: Monitoring and Alerts

## Azure Monitoring

Configured Azure Monitor and VM insights to track: 

- CPU utilization
- Memory utilization
- Network activity
- VM health metrics

### Alert Rules Configured

- High CPU usage alerts
- Resource health warnings
- VM availability monitoring

### Diagnostics

Reviewed Windows Event Viewer logs for:
- Failed login attempts
- System warnings
- Application errors
- Security events

# Security Configurations

Implemented foundational security practices including:

- Restricted remote access using Azure Bastion
- Configured Network Security Group (NSG) rules
- Practiced least privilege access principles
- Used separate administrative accounts
- Configured monitoring alerts for suspicious activity

---

# Troubleshooting Scenarios

## Scenario 1 | User Password Reset 

### Issue
User unable to log into workstation.

### Resolution
- Verified account status in Active Directory
- Reset password
- Forced password change at next login

---

## Scenario 2 | Locked Account

### Issue 
Multiple failed login attempts locked user account.

### Resolution
- Identified lockout in Active Directory
- Unlocked user account
- Reviewed login attempt logs

---

## Scenario 3 | Group Policy Issue

### Issue
User states company desktop wallpaper and password policy are not updating after login.

### Resolution
- Verified user OU placement
- Checked applied policies
- Reviewed Group Policy Configuration
- Re-Enabled the GPO link
- Forced Group Policy Update
- Verfied Successful policy application

---

# Lab Outcomes

- Successfully deployed and configured Azure-based infrastructure
- Installed and configured Active Directory Domain Services
- Created Organizational Units and multiple user accounts
- Simulated enterprise IT support workflows
- Configured monitoring and alerting
- Practiced remote administration using Azure Bastion
- Documented troubleshooting procedures
- Gained hands-on cloud and systems administration experience

---

# Future Improvements 

Planned enhancements for future development:

- Implement Azure Entra ID integration
- Configure Group Policy Objects (GPOs)
- Automate deployments using Terraform
- Add Powershell automation scripts
- Configure Role-Based Access Control (RBAC)
- Implement Azure Backup and disaster recovery
- Add Log Analytics workspace integration
- Configure Microsoft Sentinel SIEM
- Create multi-VM segmented network architecture
- Implement GitHub Actions CI/CD workflows

---
