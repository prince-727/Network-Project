# Network Assignment Using Cisco Packet Tracer

This project demonstrates the design, configuration, and testing of a departmental network for **TechNova Ltd** using Cisco Packet Tracer. It connects the IT, Sales, and HR departments through a router and switches, with a central server providing network services. The project also implements DHCP and Access Control Lists (ACLs) to manage IP address allocation, control departmental access, and maintain access to essential server services.

## Table of Contents

- [Project Overview](#project-overview)
- [Network Topology](#network-topology)
- [Tools and Technologies](#tools-and-technologies)
- [Configuration Steps](#configuration-steps)
- [Results and Findings](#results-and-findings)
- [Author](#author)

## Project Overview

The purpose of this project is to design and implement a functional enterprise network for **TechNova Ltd** using Cisco Packet Tracer. The network connects three departments—IT, Sales, and HR—and provides controlled communication between them.

The main objectives are to:

- Design a network topology connecting the IT, Sales, and HR departments.
- Configure IP addressing for departmental devices and the central server.
- Implement **Dynamic Host Configuration Protocol (DHCP)** for automatic IP address allocation.
- Configure DHCP relay functionality using IP helper addresses for the Sales and HR departments.
- Configure **File Transfer Protocol (FTP)** and HTTP services on the server.
- Apply **Access Control Lists (ACLs)** to restrict traffic from the Sales department to the IT department while preserving access to server services.
- Test network connectivity using `ipconfig` and `ping`.

## Network Topology

The network consists of three departmental LANs connected through a central router. Each department has a switch connecting its end devices to the network. A central server is located in the IT department and provides network services.

### Network Components

- **IT Department:** Contains client devices and the central TechNova Ltd server.
- **Sales Department:** Contains client devices connected through a departmental switch.
- **HR Department:** Contains client devices connected through a departmental switch.
- **Router:** Connects the departmental networks and applies routing and access-control policies.
- **Switches:** Connect departmental devices to the network and provide connectivity to the router.
- **Server:** Provides DHCP, FTP, and HTTP services.

### IP Addressing Scheme

The documented network includes the following subnets:

| Department or Network | IP Address Range | Purpose |
|---|---|---|
| IT Department | `192.168.10.0/24` | IT clients and departmental resources |
| Sales Department | `192.198.20.0/24` | Sales clients |
| HR Department | Exact subnet not specified in the document | HR clients |
| Central Server | Exact IP address not specified in the document | DHCP, FTP, and HTTP services |

**Note:** The Sales subnet is recorded as `192.198.20.0/24` in the project documentation. The exact IP addresses of the server, router interfaces, and HR subnet are not specified in the extracted text.

### Network Connectivity and Access Control

- The departmental switches connect to the central router.
- The IT department uses DHCP to obtain IP configuration automatically.
- IP helper addresses are configured to support DHCP for the Sales and HR departments.
- An ACL on the router prevents the Sales subnet from accessing the IT subnet while allowing access to server services and other permitted traffic.
- Connectivity tests verify communication between departments and confirm the intended access restrictions.

## Tools and Technologies

- **Cisco Packet Tracer:** Network topology design, device configuration, and simulation.
- **Router:** Inter-network routing and ACL enforcement.
- **Network switches:** Departmental LAN connectivity.
- **Server:** Centralized network services.
- **DHCP:** Automatic IP address assignment.
- **IP helper address:** DHCP relay functionality for departmental networks.
- **FTP:** File transfer service configured on the server.
- **HTTP:** Web service accessible to authorized network clients.
- **Access Control Lists (ACLs):** Traffic filtering and departmental access restrictions.
- **Command Prompt:** Network configuration and connectivity verification.
- **`ipconfig`:** Verification of assigned IP addresses.
- **`ping`:** Testing connectivity between network devices.

## Configuration Steps

1. **Design the network topology.**
   - Create the TechNova Ltd network in Cisco Packet Tracer.
   - Add the router, departmental switches, client PCs, and central server.
   - Connect the IT, Sales, and HR departmental networks to the router.

2. **Configure departmental IP addressing.**
   - Assign IP configurations to the departmental devices.
   - Configure the IT subnet as `192.168.10.0/24`.
   - Configure the Sales subnet as documented: `192.198.20.0/24`.
   - Configure the HR subnet and remaining device addresses according to the topology.

3. **Configure the central server.**
   - Assign an IP address and the required network settings to the server.
   - Enable DHCP functionality for automatic address allocation.
   - Configure the FTP service.
   - Enable the HTTP service to provide web access.

4. **Configure DHCP for the IT department.**
   - Set the IT clients to obtain their IP configuration automatically.
   - Verify that clients receive their addresses from the DHCP server.
   - Use `ipconfig` to confirm the assigned configuration.

5. **Configure DHCP relay for the Sales and HR departments.**
   - Configure IP helper addresses on the appropriate router interfaces to forward DHCP requests to the server.
   - Verify that clients in both departments can obtain IP addresses automatically.

6. **Connect the departmental switches to the router.**
   - Establish connections between the IT, Sales, and HR switches and the router.
   - Verify that the relevant interfaces and links are operational.

7. **Test basic network connectivity.**
   - Use `ipconfig` to inspect client IP configurations.
   - Use `ping` to test connectivity between devices.
   - Confirm that the IT department's documented ping test receives four packets, with four received and zero lost.

8. **Configure the Access Control List (ACL).**
   - Apply an ACL on the router to prevent the Sales network (`192.198.20.0/24`) from reaching the IT network (`192.168.10.0/24`).
   - Preserve access to the server's HTTP service and other traffic permitted by the configured policy.
   - Verify that the restrictions apply to the intended destination rather than blocking all interdepartmental communication.

9. **Verify the access-control policy.**
   - Ping an IT PC from a Sales PC and confirm that the connection is blocked.
   - Ping an HR PC from a Sales PC and confirm that communication remains successful.
   - Test HTTP access from the Sales department to the server to confirm that the web service remains accessible.

## Results and Findings

The project successfully demonstrates the implementation and testing of a departmental network in Cisco Packet Tracer.

### Key Results

- **Network topology:** The IT, Sales, and HR departments were connected through departmental switches and a central router.
- **IP addressing:** IP configurations were established for departmental devices and the server.
- **DHCP:** Automatic IP address assignment was demonstrated for IT clients, with IP helper addresses configured for the Sales and HR departments.
- **Connectivity verification:** The documented IT ping test reported four packets received and zero packets lost.
- **Access control:** The router ACL blocked traffic from the Sales network to the IT network, with the Sales-to-IT ping returning `Destination Host unreachable`.
- **Interdepartmental communication:** A successful ping from Sales to HR demonstrated that the ACL did not block all communication between departments.
- **Server accessibility:** A successful HTTP access test from the Sales department confirmed that the server's web service remained accessible despite the restrictions on access to the IT network.
- **FTP configuration:** The server's FTP service was configured as part of the network setup.

### Findings

The project demonstrates how DHCP simplifies client configuration and how IP helper addresses support DHCP across routed networks. It also shows how router ACLs can enforce departmental access restrictions while allowing explicitly permitted services, such as HTTP, to remain accessible.

The connectivity tests provide evidence that the configured network supports the intended communication paths and restrictions. The document does not provide a complete numerical record of every device's IP configuration or all FTP and HTTP service tests.

## Author

**Name:** Prince Atinyo

**Project:** Network Project Using Cisco Packet Tracer
