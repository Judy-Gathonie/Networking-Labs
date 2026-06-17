# Network Design for Accounts and Delivery Departments

This Cisco Packet Tracer project demonstrates the design and implementation of a small enterprise network connecting the **Accounts** and **Delivery** departments.

## Objectives
- Provide network connectivity for two PCs in each department.
- Segment departments into separate subnets.
- Enable communication between departments through a router.
- Use the 192.168.40.0 network block.

## Network Devices
- 1 Router  
- 2 Cisco 2960 Switches  
- 4 PCs  

## IP Addressing

| Department | Subnet | Gateway |
|------------|---------|----------|
| Accounts | 192.168.40.0/25 | 192.168.40.1 |
| Delivery | 192.168.40.128/25 | 192.168.40.129 |

## Features
- Subnetting using /25 networks  
- Inter-subnet routing  
- Static IP configuration  
- End-to-end connectivity verification using ping  

## Verification
Successful ICMP tests confirm communication between devices in different departments through the router.

## File
- `SimpleNetwork.pkt` – Cisco Packet Tracer topology and configuration
