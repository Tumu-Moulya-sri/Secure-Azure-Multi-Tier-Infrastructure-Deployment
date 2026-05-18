# Project Overview

This project demonstrates the deployment of a secure Ubuntu Virtual Machine in Microsoft Azure using cloud networking and security best practices.
The project includes:
- Azure Virtual Machine deployment
- Azure Virtual Network (VNet) configuration
- Subnet segmentation
- Public and private IP configuration
- Network Security Group (NSG) firewall rules
- SSH-based remote access
- Apache web server deployment
- Hosting a custom HTML webpage from Azure

This project was created as a hands-on cloud networking and cloud security learning project.

# Architecture diagram:
<img width="1003" height="724" alt="architecture-diagram" src="https://github.com/user-attachments/assets/bc2bc196-80fa-4735-bc38-b1b26db450b4" />

# Azure Services Used

|  Azure service                |            Purpose                     |
|  -------------                |        -------------                   |
| Resource Group                |  Logical container for Azure resources |
| Virtual Machine               |  Cloud-based Ubuntu Linux serve        |
| Virtual Network (VNet)        |  Private cloud networks                |
| Subnets                       |  Network segmentation inside VNet      |
| Network Security Group (NSG)  |  Firewall rules management             |
| Public IP                     |  Internet accessibility                |
| Private IP                    |  Internal Azure communication          |


# Networking Concepts Implemented
- Virtual Network (VNet): A Virtual Network was created to simulate a private enterprise cloud network inside Azure.

- Subnet Segmentation: Two subnets were created:
Subnet-Frontend
Subnet-Backend
This demonstrates basic network segmentation and separation of infrastructure.

- Public vs Private IP: The Virtual Machine was assigned:
Public IP for internet access and SSH connectivity
Private IP for internal Azure network communication

- NSG Firewall Rules: Inbound firewall rules were configured using Azure NSG.

Allowed ports:

|  Port	 |      Purpose       | 
| ------ |    ------------    |
|   22	 | SSH Remote Access  |
|   80	 | HTTP Web Traffic   |


# Security Concepts Demonstrated
- SSH key-based authentication
- Controlled inbound access
- Network segmentation
- Firewall configuration
- Minimizing unnecessary exposed ports
- Understanding cloud attack surfaces

# Apache Web Server Deployment
Apache2 web server was installed on the Ubuntu VM.
A custom HTML webpage was hosted and made accessible publicly using the VM's public IP address.

# Screenshots:
# Resource group:
<img width="1452" height="810" alt="resource-group" src="https://github.com/user-attachments/assets/ef3706e8-cafe-4539-af90-0d539c442738" />

# Virtual Network
<img width="1462" height="662" alt="virtual-network" src="https://github.com/user-attachments/assets/6747a79e-3f73-4449-9dbb-ca8d6d317851" />

# Subnets
<img width="1242" height="455" alt="subnets" src="https://github.com/user-attachments/assets/0b5c8ebc-39a0-4785-8070-957f2d943eec" />

# VM Overview
<img width="1790" height="692" alt="vm-overview" src="https://github.com/user-attachments/assets/a751d811-ba78-46a7-b27f-14c3378a4b37" />

# NSG Rules
<img width="1812" height="537" alt="networking-rules" src="https://github.com/user-attachments/assets/b11c68e9-5544-48c2-aa35-2142fa699ac6" />

# SSH Access
<img width="1277" height="482" alt="ssh-terminal" src="https://github.com/user-attachments/assets/1a740bd5-176a-42ce-8543-b1275630355b" />

# Hosted webpage
<img width="1907" height="927" alt="apache-homepage" src="https://github.com/user-attachments/assets/0e821292-df89-4193-babb-6bb5f03552eb" />

# Conclusion
This project provided practical hands-on experience with Microsoft Azure cloud infrastructure, networking, Linux administration, and foundational cloud security concepts.
It demonstrates how cloud resources, networking, firewall rules, and web hosting work together in a real-world environment.
