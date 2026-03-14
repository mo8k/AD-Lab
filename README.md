 ## Project Overview

This project documents the deployment of a Windows-based Active Directory environment within a Proxmox VE cluster. The goal is to demonstrate core SysAdmin skills: virtualization, networking, and identity management.

# 🏗 Architecture & Topology

To simulate a real-world enterprise environment, the lab is hosted on an isolated virtual network.

Hypervisor: Proxmox VE (4-node cluster)

Network Bridge: LabNet (Isolated / No Gateway) (VXLAN configured throughout Lab enviorment)

Domain Controller (DC01): Windows Server 2022

IP: 172.xx.xx.x

Roles: AD DS, DNS, DHCP

Client Machine (CL01): Windows 10 Enterprise

IP: 172.xx.xx.x

Domain: lab.local

[ Proxmox Host ]
       |
    [ vmbr1 ] <--- Isolated Virtual Switch
       |
    +--+----------------+
    |                   |
 [ DC01 ]            [ CL01 ]
(172.16.0.1)        (172.16.0.10)

