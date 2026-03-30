# Active Directory Lab Setup

## Objective
To build and configure a Windows Active Directory environment for centralized user management and security policy enforcement.

##  Tools Used
- Windows Server 2022
- Windows 11 Clients
- VirtualBox
- Mobaxterm

##  Network Configuration
- Network: 192.168.56.0/24
- Domain Controller IP: 192.168.56.10
- Client 1 IP: 192.168.56.20
- Client 2 IP: 192.168.56.21

##  Lab Setup
- 1 Domain Controllers
- 2 Client Machines
- Internal network (isolated lab)

## Configuration Steps

### 1. Installed Windows Server
- Set static IP address
- Renamed server

### 2. Installed Active Directory Domain Services (AD DS)
- Promoted server to Domain Controller
- Created domain: lab.local

### 3. Created Users and Groups
- Added multiple users
- Organized into groups

### 4. Joined Client Machines to Domain
- Configured DNS to point to Domain Controller
- Successfully joined domain

### 5. Configured Group Policy
- Enforced password policy
- Account lockout settings

## 📸Screenshots
(Add your screenshots here later)

## 🔍 Key Learnings
- How Active Directory manages users centrally
- Importance of DNS in domain environments
- How Group Policy enforces security

##  Disclaimer
This lab was conducted in a controlled virtual environment for educational purposes only.
