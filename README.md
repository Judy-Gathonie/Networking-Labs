# Network Design for Accounts and Delivery Departments

This Cisco Packet Tracer project demonstrates the design and implementation of a small enterprise network connecting the **Accounts** and **Delivery** departments.

## Objectives
- Separate departments into distinct subnets for security and traffic control.
- Enable cross-department communication through an intermediate router.
- Provide reliable network connectivity for two PCs and one printer in each department.
- Allocate and optimize IP resources using the `192.168.40.0/24` block.

## Network Devices
- **1x Router:** Cisco ISR4331
- **2x Switches:** Cisco Catalyst 2960
- **4x End Devices:** Desktop PCs (2 per department)
- **2x Peripherals:** Network Printers (1 per department)

## IP Addressing Schema

| Department | Network ID | Subnet Mask | Usable Host IP Range | Default Gateway | Broadcast IP |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Accounts** | 192.168.40.0 | 255.255.255.128 (/25) | 192.168.40.2 – 192.168.40.126 | 192.168.40.1 | 192.168.40.127 |
| **Delivery** | 192.168.40.128 | 255.255.255.128 (/25) | 192.168.40.130 – 192.168.40.254 | 192.168.40.129 | 192.168.40.255 |

## Technical Features
- **Variable Length Subnet Masking (VLSM):** Segmented a class C network block using `/25` masks.
- **Inter-Subnet Routing:** Configured physical router interfaces to act as default gateways.
- **Static IP Allocation:** Manual IP assignments on all terminal host systems and network interfaces.
- **ICMP Validation:** Verified multi-hop end-to-end connectivity using standard ping tests.

## Verification
Successful ICMP echo replies confirm operational network layers and accurate configuration routing across both segments.

## Project Files
- `SimpleNetwork.pkt` – Cisco Packet Tracer network topology and configuration schema.
