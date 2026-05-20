#  Secure Azure Multi-Tier Infrastructure Deployment

## Project Overview

This project demonstrates the deployment of a secure multi-tier cloud infrastructure inside Microsoft Azure using Virtual Machines, Virtual Networks, subnets, Network Security Groups (NSGs), and backend database communication.
The architecture consists of:

- A public-facing Frontend VM hosting a website
- A private Backend VM handling backend processing and database storage
- Secure communication between frontend and backend using private IP addresses inside Azure Virtual Network

This project was built completely using the Azure Portal and Linux administration through SSH

## Architecture diagram:
<img width="1408" height="768" alt="architecture-diagram-2" src="https://github.com/user-attachments/assets/83269cb7-5d80-48d3-8f30-79417c005048" />


## Azure Services Used

|  Azure service                |            Purpose                     |
|  -------------                |        -------------                   |
| Resource Group                |  Logical container for Azure resources |
| VM-Frontend-01 Virtual Machine|  Public-facing Ubuntu VM               |
| VM-Backend-01 Virtual Machine |  Private Ubuntu VM without public IP   |
| Virtual Network (VNet)        |  Private cloud networks                |
| Subnets                       |  Network segmentation inside VNet      |
| Network Security Group (NSG)  |  Firewall rules management             |
| Public IP                     |  Internet accessibility                |
| Private IP                    |  Internal Azure communication          |


## Networking Concepts Implemented
- Virtual Network (VNet): A Virtual Network was created to simulate a private enterprise cloud network inside Azure.

- Subnet Segmentation: Two subnets were created:
Subnet-Frontend
Subnet-Backend
This demonstrates basic network segmentation and separation of infrastructure.

- Public vs Private IP: The Virtual Machine was assigned:
Public IP for internet access and SSH connectivity
Private IP for internal Azure network communication

- NSG Firewall Rules: Inbound firewall rules were configured using Azure NSG.

- Secure Backend Isolation

Allowed ports for Frontend VM:

|  Port	 |      Purpose       | 
| ------ |    ------------    |
|   22	 | SSH Remote Access  |
|   80	 | HTTP Web Traffic   |

Allowed ports for Backend VM:

|   Port	 |         Purpose          | 
|  ------  |       ------------       |
|    22	   | SSH Remote Access        |
|   5000	 | Python backend service   |


## Security Concepts Demonstrated
- Backend VM hidden from public internet
- Restricted inbound traffic using NSGs
- SSH authentication using key pairs
- Separation of frontend and backend systems
- Internal-only backend communication

## Application Workflow

1. User accesses frontend website using Frontend VM public IP.
2. Apache web server serves the frontend webpage.
3. User submits form data.
4. Frontend VM internally communicates with Backend VM using private IP.
5. Backend Python server processes the request.
6. Data is stored in SQLite database inside Backend VM.
7. Backend server responds back to frontend.

# Screenshots:
## Resource group:
<img width="1452" height="810" alt="resource-group" src="https://github.com/user-attachments/assets/ef3706e8-cafe-4539-af90-0d539c442738" />

## Virtual Network
<img width="1462" height="662" alt="virtual-network" src="https://github.com/user-attachments/assets/6747a79e-3f73-4449-9dbb-ca8d6d317851" />

## Subnets
<img width="1242" height="455" alt="subnets" src="https://github.com/user-attachments/assets/0b5c8ebc-39a0-4785-8070-957f2d943eec" />

## Frontend VM Overview
<img width="1790" height="692" alt="vm-overview" src="https://github.com/user-attachments/assets/a751d811-ba78-46a7-b27f-14c3378a4b37" />

## Backend VM overview
<img width="1740" height="842" alt="vm2-overview" src="https://github.com/user-attachments/assets/8a7da2d8-0af9-4000-86ff-2679363f39bb" />

## NSG Rules
<img width="1812" height="537" alt="networking-rules" src="https://github.com/user-attachments/assets/b11c68e9-5544-48c2-aa35-2142fa699ac6" />

<img width="1842" height="592" alt="nsg-rules-vm2" src="https://github.com/user-attachments/assets/e2798bae-3718-46d9-9ca6-9c321700f18a" />

## SSH Access
<img width="1277" height="482" alt="ssh-terminal" src="https://github.com/user-attachments/assets/1a740bd5-176a-42ce-8543-b1275630355b" />

## Hosted webpage
<img width="1906" height="942" alt="front-end" src="https://github.com/user-attachments/assets/614c5e79-df2d-45c2-bfeb-750e6cdff9d6" />

## Backend Database Communication
<img width="767" height="185" alt="backend-vm" src="https://github.com/user-attachments/assets/15e35cf0-498b-4682-bd61-e420bf693ead" />



