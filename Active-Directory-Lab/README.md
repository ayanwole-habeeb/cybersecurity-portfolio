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
-Two Domain Controllers
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
- abj01-wc-wk01 (Workstation 1)
- abj01-wc-wk02 (Workstation 2)

### 3.Static IP Configuration
Servers were assigned static IP addresses to ensure:
- Network stability
- Reliable DNS resolution
- Proper Active Directory functionality

### Screenshots
### Domain Controller 1
<img width="1365" height="767" alt="Screenshot 2026-03-31 102325" src="https://github.com/user-attachments/assets/f4593ba3-616b-45e8-9979-1aec350b9f5a" />

### Domain Controller 2
<img width="1365" height="767" alt="Screenshot 2026-03-31 102651" src="https://github.com/user-attachments/assets/fdcf4e92-6db9-4477-a37c-8cf1ac8ab327" />

### Server 1
<img width="1365" height="767" alt="Screenshot 2026-03-31 103103" src="https://github.com/user-attachments/assets/f37ccc68-3b01-44b5-be69-79e27fa180ba" />

### Server 2
<img width="1358" height="767" alt="Screenshot 2026-03-31 103348" src="https://github.com/user-attachments/assets/eacf1780-0332-4fa1-83f8-a72f6b683966" />

### workstation 1
<img width="1365" height="767" alt="Screenshot 2026-03-31 161400" src="https://github.com/user-attachments/assets/22a8dedd-28e1-4fd4-b87d-7a0645fb39e2" />

### workstation 5
<img width="1365" height="767" alt="Screenshot 2026-03-31 212031" src="https://github.com/user-attachments/assets/48cf97e2-cdaf-4ceb-95ce-f1f428b42a76" />




##  Disclaimer
This lab was conducted in a controlled virtual environment for educational purposes only.
