# Active Directory Lab Setup

## Objective
To build and configure a Windows Active Directory environment for centralized user management and security policy enforcement.

##  Tools Used
- Windows Server 2022
- Windows 11 Clients
- VirtualBox
- Mobaxterm
- SmartBox Router

  ##  Lab Setup
  Two Domain Controllers
- Five Client Machines
- Five other Servers
  ### VirtualBox Manager
<img width="1365" height="767" alt="Screenshot 2026-04-01 135527" src="https://github.com/user-attachments/assets/6e7aa804-e2f7-432e-b1f2-75a5a1558f22" />

  
##  Configuration
### 1. Network Configuration
- Network: 192.168.1.0/24
- subnetmask: 255.255.255.0
- Choosen Router DHCP IP POOL : 192.168.1.20 - 192.168.1.20.43
- Router IP :192.168.1.19
- DNS / Defualt Gateway IP : 192.168.1.19
  ### IP Addressing Scheme
<img width="841" height="508" alt="Screenshot 2026-04-01 120313 - Copy" src="https://github.com/user-attachments/assets/94c9a281-aede-47cf-8d24-862bb0de45f1" />

### Router Settings
<img width="1155" height="689" alt="Screenshot 2026-04-01 121812" src="https://github.com/user-attachments/assets/e0a73f1b-f2d7-475c-9440-7c9375dea207" />

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

## Screenshots
(Add your screenshots here later)



##  Disclaimer
This lab was conducted in a controlled virtual environment for educational purposes only.
