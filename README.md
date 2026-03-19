This project has been created as part of the 42 curriculum by jili.

# Description
This project is about the basics of computer networking. We will learn how to configure IP adresses, connect devices through a router, and understand the role of a gateway within a network.

## KEY POINTS:
1. basic concepts
2. convert demical number to binary number and convert binary number to demical number

# Instructions
1. First, download the ffle attached to the project’s page
2. Then, extract the files into any folder of your choice.
3. run “python3 -m http.server 49242” in the terminal of this folder. 
5. Copy the lien http://localhost:49242 to the google browser. This step will launch a web server and open the interface in the google browser.
6. practice by entering your login in the field to use your personal configuration.
7. use the "evaluation" tab to generate a random configuration, also suitable for evaluations
8. There are 10 levels for training. For each level, a non-fonctioning network diagram is displayed. There are two buttons we can use :[Check again] to verify whether your conffguration is correct;[Get my config] to download your conffguration whenever you need to; you will
need it when submitting your assignment.When you have successfully completed a level, a new button will appear. Click this button to proceed to the next level.
	
# Resources
## Local Area Network(LAN) VS Subnet 
1. A LAN is a physical or logical group of devices​ connected within a limited geographic area (e.g., a home, office, or campus). Key traits:🅰️Devices in a LAN can communicate directly (e.g., via switches or Wi-Fi).🅰️Traditionally, a LAN might use a single IP address range (e.g., 192.168.1.0/24).
2. A subnet is a logical subdivision of an IP network, created by partitioning a larger network (like a LAN) using a subnet mask. Key traits: 🅰️Divides a LAN into smaller segments for efficiency, security, or management (e.g., 192.168.1.0/28and 192.168.1.16/28). 🅰️Requires a router​ to communicate between subnets (as seen in NetPractice’s router configurations).🅰️Subnetting reduces broadcast traffic and isolates segments (e.g., separating departments in an office).
   
## TCP/IP adresse (internet Protocol Address)
1. IP adresse is an identifier for your computer, it just like a home adress for your computer on a network. 
2. His format is four numbers seperated by dots(e.g., 192.168.1.1). These four numbers you see are demical representations of binary numbers. So each number is called an "octet" (8 binary digits), and the range for each number is 0 to 255 (because 2⁸=256 possible values).
3. 127.0.0.xis a loopback address​ (reserved for internal testing on a single device)；These IPs cannot​ be used for communication between separate hosts (like Host C and Host D).
### Usable Host Range：
   In computer networking, Network Address​ and Broadcast Address​ are two reserved IP addresses within a subnet that serve specific purposes:
1. Network Address ->​ The first IP address in a subnet, used to identify the network itself. It Represents the entire subnet (e.g., 192.168.1.0/25) and Cannot be assigned to any device.
How to identify: All host bits set to 0(e.g., 192.168.1.0in 192.168.1.0/25).
2. Broadcast Address -> The last IP address in a subnet, used to send data to all devices in the network. It Allows one-to-all communication (e.g., ARP requests) and Cannot be assigned to any device.
How to identify: All host bits set to 1(e.g., 192.168.1.127in 192.168.1.0/25).
### useful links:
https://en.wikipedia.org/wiki/IP_address  
## Subnet masks 
1. Subnet adress defines which part of the IP adress id the NETWORK and which is the DEVICE.
2. A subnet mask (e.g., 255.255.255.224 or /27) splits an IP address into:
  		~ Network portion: Bits where the subnet mask is 1.
		~ Host portion: Bits where the subnet mask is 0.
3. There are two representations of Subnet Mask:
		~ Dotted-demical notation, eg. 255.255.255.224
		~ CIDR (Classless Inter-Domain Routing) notation, eg. /27. It tells you how many bits in an IP address are used for the network portion​ (the rest are for hosts).
4. Devices can communicate directly if their IPs match the subnet (that means they are in the same network); If they are in different networks, they must go through a gateway(router) to commununicate.
5. All devices on the same cable/wireless must be in the same network.

### ATTENTION:
IP Addresses & Subnet Masks Are Binary Numbers in Decimal Form: An IPv4 address​ (e.g., 192.168.1.1) is a 32-bit binary number split into 4 octets (8 bits each), displayed in decimal​ for readability. IP: 192.168.1.1 → 11000000.10101000.00000001.00000001
### useful links:
https://www.calculator.net/ip-subnet-calculator.html  
https://en.wikipedia.org/wiki/Subnet  

## default gateways
1. Default gateway = the IP of the router interface that is in the same subnet as your device
2. All devices within the same Subnet share the same Default Gateway — which is the IP address of the router's interface that lives inside that Subnet.
### useful links
https://en.wikipedia.org/wiki/Default_gateway  


## swiches
1. In computer networking, a switch​ is a device that connects multiple devices (like computers, printers, or other switches/routers) on a local area network (LAN). Its primary job is to forward data packets​ to the correct destination based on the MAC address​ (Media Access Control address) of the receiving device.

## network loop
1. A network loop occurs when data packets circulate endlessly between network devices due to redundant paths and misconfigurations. This can cause boardcast storms (Uncontrolled flooding of traffic) and performance degradation (congestion and packet loss)

## router 
1. Routers connect different subnets (or networks) and enable communication between devices on separate subnets. : you cannot route between two hosts on the same subnet using a router.
### Rules of router interfaces
A router interface is like a "door" into a specific subnet. To send a packet somewhere, the router must have a door that opens into that neighborhood.
1. Each Interface Belongs to Exactly One Subnet: When you assign an IP + Mask to an interface, that interface joins that subnet.
2. Two Routers Connect via a Shared Subnet : For R1 and R2 to talk to each other, one interface from each router must be in the same subnet.
## OSI layers
The OSI (Open Systems Interconnection) model​ is a conceptual framework that standardizes the functions of a telecommunication or computing system into seven abstraction layers.
### OSI Model Layers
1. Physical Layer (Layer 1) : Deals with raw bit transmission over physical media(eg. cables, wifi signals).
2. Data Link Layer (Layer 2) : Manages MAC adresses and local network communication(eg. switches).
3. Network Layer (Layer 3) : Handles IP adressing and routing between networks(eg. routers).
4. Transport Layer (Layer 4) : Ensures end-to-end communication(eg.TCP/UDP).
5. Session Layer (Layer 5): Manages connections between applications.
6. Presentation Layer (Layer 6): Translates data formats (eg. encryption)
7. Application Layer (Layer 7) : Interfaces with applications(eg. HTTP. FTP).

### Errors Log
1. “multiple interface match” (Netpractice_level 4): Router R has multiple interfaces (R1, R2, R3) all in the same subnet 92.31.111.0/24 — so when a packet arrives for Host B (92.31.111.193), the router doesn't know which interface to use → multiple interface match.
.



