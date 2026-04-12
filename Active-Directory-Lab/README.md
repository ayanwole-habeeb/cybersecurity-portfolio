# Active Directory Lab Setup

## Objective
To build and configure a Windows Active Directory environment for centralized user management and security policy enforcement.

##  Tools Used
- Windows Server 2022
- Windows 11 Clients
- VirtualBox
- Mobaxterm
- SmartBox Router

##  Network Architecture

This lab uses a dual-network design:

- External Network (DHCP) for internet and remote access
- Internal Network (Host-Only) for Active Directory and server communication

Each server is configured with:
- Static IP (internal network)
- DHCP IP (external network)

  ##  Lab Setup
- Two Domain Controllers
- Five Client Machines
- Five other Servers
  
  ### VirtualBox Manager
<img width="1365" height="767" alt="Screenshot 2026-04-01 135527" src="https://github.com/user-attachments/assets/6e7aa804-e2f7-432e-b1f2-75a5a1558f22" />

  
##  Configuration
### 1. IP Address Planning and Subnetting
Designed and implemented IP addressing scheme using subnetting and allocated 24 IP to all virtual machines in my lab,using the SmartBox router DHCP pool.
- Network: 192.168.1.0/24
- subnetmask: 255.255.255.0
- Choosen Router DHCP IP POOL : 192.168.1.20 - 192.168.1.20.43
- Router IP :192.168.1.19
- DNS / Defualt Gateway IP : 192.168.1.19
  ### IP Addressing Scheme
<img width="841" height="508" alt="Screenshot 2026-04-01 120313 - Copy" src="https://github.com/user-attachments/assets/94c9a281-aede-47cf-8d24-862bb0de45f1" />

### Router Settings
<img width="1155" height="689" alt="Screenshot 2026-04-01 121812" src="https://github.com/user-attachments/assets/e0a73f1b-f2d7-475c-9440-7c9375dea207" />

### 2. Machine Renaming
All systems were renamed to follow a structured enterprise naming convention:
- abj01-ws-dc01 (Domain Controller 1)
- os01-ws-dc02 (Domain Controller 2)
- abj01-ws-sv01 (Server 1)
- abj01-ws-sv02 (Server 2)
- abj01-ws-sv03 (Server 3)
- abj01-ws-sv04 (Server 4)
- abj01-ws-sv05 (Server 5)
- abj01-wc-wk01 (Workstation 1)
- abj01-wc-wk02 (Workstation 2)
- abj01-wc-wk03 (Workstation 3)
- abj01-wc-wk04 (Workstation 4)

### 3.Static IP Configuration
To ensure stability and proper communication across the lab, all Windows Servers were configured with static IP addresses.
- abj01-ws-dc01 (Domain Controller 1) : 172.30.55.20
- os01-ws-dc02 (Domain Controller 2) : 172.30.55.57
- abj01-ws-sv01 (Server 1) : 172.30.55.18
- abj01-ws-sv02 (Server 2) : 172.30.55.12
- abj01-ws-sv03 (Server 3) : 172.30.55.89
- abj01-ws-sv04 (Server 4) : 172.30.55.34
- abj01-ws-sv05 (Server 5) : 172.30.55.42

#### 4. MobaXterm (Centralized Access Tool)
- Used MobaXterm to manage both RDP and SSH sessions
- Created saved sessions for quick access to all machines



### Screenshots
### Remote connection using MobaXterm to abj01-ws-dc01 (Domain Controller 1) : Static ip (172.30.55.20)
<img width="1365" height="767" alt="Screenshot 2026-04-06 050150" src="https://github.com/user-attachments/assets/11700a8c-31b8-4f95-b530-d1d416ca6059" />

### abj01-ws-sv05 (Server 5) : Static ip ( 172.30.55.42 )
<img width="1355" height="767" alt="Screenshot 2026-04-06 045812" src="https://github.com/user-attachments/assets/b206ba4a-517e-4515-9df8-370ee2b18fa7" />

### abj01-ws-sv02 (Server 2) : Static ip ( 172.30.55.12 )
<img width="1365" height="767" alt="Screenshot 2026-04-06 040115" src="https://github.com/user-attachments/assets/0e0cbbd7-c0fe-43ce-ab7f-90b2fe3a08d2" />

##  Active Directory Deployment

- Installed Active Directory Domain Services 
- Promoted abj01-ws-dc01 to Domain Controller
- Configured new forest: beecipher.local
- Configured DNS Forward and Reverse Lookup Zones
- Verified DNS resolution using nslookup

### Screenshots
### Active Directory Domain Services Installed
<img width="1365" height="767" alt="Screenshot 2026-04-08 135710" src="https://github.com/user-attachments/assets/492d5a75-442d-4625-9cdc-3afbe1a4a3ef" />

### DNS Forward and Reverse Lookup Zones Configured
<img width="1365" height="767" alt="Screenshot 2026-04-08 140603" src="https://github.com/user-attachments/assets/79a2f9b4-37bf-4060-b013-cd5f2832e7a5" />

### DNS Confirmation, using nslookup 
<img width="1365" height="767" alt="Screenshot 2026-04-08 132425" src="https://github.com/user-attachments/assets/4a49f804-67f5-4280-bab2-7bff473dc1ea" />

## Active Directory User and Domain Integration
In this phase of the lab, I implemented user account management and integrated all servers and workstations into the domain environment.

### User Account Configuration

Created different types of Active Directory accounts:

- **Enterprise Admin** → For full control across the forest
- **Domain Admin** →For full control within the domain
- **Standard Domain Users** → Limited access for daily operations,user will only have access to workstations

### Domain Joining
- Successfully joined all Windows Servers to the domain
- Joined Windows client workstations to the domain

### Authentication Testing
- Logged into domain-joined machines using domain user credentials
- Verified access levels based on account types

### Outcome
- Centralized authentication working
- Role-based access control implemented
- All systems integrated into Active Directory domain (beecipher.local)

### Screenshots
### Active Directory Users
<img width="1365" height="767" alt="Screenshot 2026-04-11 182549" src="https://github.com/user-attachments/assets/9f16331e-985a-464a-b354-bcbd07063504" />

### Domain Controller

<img width="1365" height="767" alt="Screenshot 2026-04-11 175229" src="https://github.com/user-attachments/assets/bbdcc858-1074-4e20-9d22-f8dad00a62e0" />

### Server Domain Joining
**abj01-ws-sv01(server 1)**
<img width="1365" height="767" alt="Screenshot 2026-04-10 123450" src="https://github.com/user-attachments/assets/cd9ee017-4020-4fd5-b5db-e5222960c99c" />

**abj01-ws-sv04(server 4)**
<img width="1365" height="767" alt="Screenshot 2026-04-10 134517" src="https://github.com/user-attachments/assets/b95da775-e17a-47bc-8a4b-a2d149e0c75f" />

### Client Domain Joining
**abj01-wc-wk02(Workstation 2)**
<img width="1365" height="767" alt="Screenshot 2026-04-11 152507" src="https://github.com/user-attachments/assets/c3a5c592-ca9e-4eae-982c-08d20a7a9a60" />

**abj01-wc-wk03(Workstation 3)**
<img width="1365" height="767" alt="Screenshot 2026-04-11 154825" src="https://github.com/user-attachments/assets/5b4eab9e-80cd-412a-9158-69758ff5bb5f" />

###  Domain Login
**abj01-wc-wk03(Workstation 3)**
<img width="1361" height="767" alt="Screenshot 2026-04-11 160518" src="https://github.com/user-attachments/assets/516f2961-badb-4ecc-a16f-0d9c6039a7cf" />

**abj01-wc-wk05(Workstation 5)**
<img width="1365" height="767" alt="Screenshot 2026-04-11 174607" src="https://github.com/user-attachments/assets/5d468279-2da6-417e-aad7-d44a7c221f11" />



### Servers and workstations Joined to Active Directory domain (beecipher.local)
<img width="1365" height="767" alt="Screenshot 2026-04-11 175215" src="https://github.com/user-attachments/assets/c6a8095c-4082-41a4-826b-569fbdcb88b7" />



##  Disclaimer
This lab was conducted in a controlled virtual environment for educational purposes only.
