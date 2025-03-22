# IUB Network Design and Packet Tracer Simulation

## Project Overview
This project involves designing a network addressing scheme for **IUB** (Independent University, Bangladesh), ensuring proper allocation and usage of IP addresses for its schools, administrative divisions, and hosted websites. The network design also includes subnetting, NAT configuration, and the setup of DNS, DHCP, and SSH services for secure communication within the university network.

## Technologies and Tools Used
- **Network Simulation**: Cisco Packet Tracer
- **Protocols**: DNS, DHCP, NAT, SSH, HTTP
- **Version Control**: Git, GitHub
- **Subnetting**: Classless Addressing, CIDR
- **Operating System**: Cisco Routers and Switches for the simulation

## Challenges and Solutions
During the project, one of the challenges was ensuring efficient IP address allocation without overlap. To solve this, I carefully reviewed the network’s IP usage and implemented subnetting to ensure each subnet had the correct number of IPs while maintaining scalability for future growth.

## Real-World Application
This project simulates a real-world university network, showcasing how large organizations can efficiently manage IP addressing and ensure connectivity across multiple departments and schools. The skills demonstrated are directly applicable to IT infrastructure management, network administration, and system configuration tasks.

## Packet Tracer Simulation
Below is the Packet Tracer simulation showing the network design and connectivity.

![Network Design](images/network-design.png)


## Objectives
- Allocate IP addresses to different schools and administrative divisions.
- Implement subnetting for the administrative divisions and school networks.
- Configure network services such as DNS, DHCP, NAT, and SSH.
- Design and simulate the network on Cisco Packet Tracer with proper host communication.

## IP Address Allocation
IUB receives the IP block `171.122.12.64/26` from the ISP. The allocation of IP addresses is done as follows:

### Schools Allocation
- **Number of Schools**: 6
- **IP Allocation**: Each school is allocated 8 IP addresses.

### CITS Allocation
- **Number of IP Addresses**: 16
- **Allocation**:
  - 8 IP addresses for administrative offices
  - 8 IP addresses to host the following websites:
    - [http://iub.ac.bd](http://iub.ac.bd)
    - [http://iras.iub.edu.bd](http://iras.iub.edu.bd)
    - [http://jukti.com](http://jukti.com)

## Administrative Divisions
IUB has four administrative divisions, each with its own subnet:
1. Executive Offices
2. HR & Admin Offices
3. Accounts and Payroll Offices
4. Registration and Admissions Offices

Each division will use NAT to hide private IP blocks and will have its own DNS and DHCP services.

### Configuration
- **DNS**: Assigned to the first usable IP address of the first sub-block.
- **DHCP**: Assigned to the second usable IP address of the first sub-block.
- **Gateway**: The last usable IP address of each sub-block will be configured as the gateway.

## School Networks
Each of the 6 schools will have its own private IP block and will be divided into four sub-networks:
1. Administrative Office
2. Faculty Room
3. Classroom
4. Lab Classroom

Each subnet will use NAT and will have its own DNS and DHCP services.

### Configuration
- **DNS**: Assigned to the first usable IP address of each school subnet.
- **DHCP**: Assigned to the second usable IP address of each school subnet.
- **Gateway**: The last usable IP address of each subnet will be configured as the gateway.

## Subnetting Details
- **Number of Hosts per Subnet**: 60 hosts.
- **Classless Addressing**: Classless addressing is used to distribute IP addresses from the parent IP range allocated to each school or administrative division.
- **Packet Tracer Simulation**: The simulation will show four hosts per subnet in Cisco Packet Tracer.

## Connectivity Requirements
- **SSH Access**: Administrators must be able to access all routers and switches using the SSH protocol.
- **Host Communication**: All hosts across the network must be able to communicate with each other.

## Parent IP Block for Private Addresses
Each subnet will use a private IP block starting with:
192.168.19.10/20

## Deliverables
1. **IP Address Allocation Table**: A table showing the allocation of IP addresses to schools, administrative divisions, and websites.
2. **Subnetting Details**: A detailed breakdown of subnet masks, ranges, and key configurations (DNS, DHCP, gateway) for each subnet.
3. **Packet Tracer Simulation**: A simulation file containing:
   - Four hosts per subnet.
   - Proper connectivity between hosts.
   - DNS, DHCP, HTTP
   -  configurations.
   - NAT, SSH configurations for secure access.

## Files and Directories
- **ip_address_calculations.xlsx**: Contains the IP allocation details for schools, administrative divisions, website and the subnetting information for all the subnets in the network.
- **packet_tracer_project.pkt**: The Cisco Packet Tracer simulation file showcasing the network design and configuration.

## Setup Instructions
To run the simulation on Cisco Packet Tracer:
1. Download and install Cisco Packet Tracer from the [official website](https://www.netacad.com/courses/packet-tracer).
2. Open the `.pkt` file in Cisco Packet Tracer to view and simulate the network design.
3. Verify connectivity and services (DNS, DHCP, HTTP) between hosts.

## Reproduce This Project
1. Clone this repository:
   ```bash
   git clone https://github.com/ashrafulcs/Packet-Tracer-Project.git
