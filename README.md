This project has been created as part of the 42 curriculum by jili.

*** Description ***
This project is about the basics of computer networking. We will learn how to configure IP adresses, connect devices through a router, and understand the role of a gateway within a network.

KEY POINTS:
	* basic concepts
	* convert demical number to binary number and convert binary number to demical number

*** Instructions ***
1. first run “python3 -m http.server 49242”
2. Copy the lien http://localhost:49242 to the google browser
	
*** Resources ***

# TCP/IP adresse (internet Protocol Address)
1. IP adresse is an identifier for your computer, it just like a home adress for your computer on a network. 
2. His format is four numbers seperated by dots(e.g., 192.168.1.1). These four numbers you see are demical representations of binary numbers. So each number is called an "octet" (8 binary digits), and the range for each number is 0 to 255 (because 2⁸=256 possible values).
3. 127.0.0.xis a loopback address​ (reserved for internal testing on a single device)；These IPs cannot​ be used for communication between separate hosts (like Host C and Host D).
4. Usable Host Range：
   In computer networking, Network Address​ and Broadcast Address​ are two reserved IP addresses within a subnet that serve specific purposes:
   Network Address ->​ The first IP address in a subnet, used to identify the network itself. It Represents the entire subnet (e.g., 192.168.1.0/25) and Cannot be assigned to any device.
How to identify:
All host bits set to 0(e.g., 192.168.1.0in 192.168.1.0/25).
		Broadcast Address	-> The last IP address in a subnet, used to send data to all devices in the network. It Allows one-to-all communication (e.g., ARP requests) and Cannot be assigned to any device.
How to identify:
All host bits set to 1(e.g., 192.168.1.127in 192.168.1.0/25).
6. 
	
# Subnet masks 
1. Subnet adress defines which part of the IP adress id the NETWORK and which is the DEVICE.
2. A subnet mask (e.g., 255.255.255.224 or /27) splits an IP address into:
  		~ Network portion: Bits where the subnet mask is 1.
		~ Host portion: Bits where the subnet mask is 0.
3. There are two representations of Subnet Mask:
		~ Dotted-demical notation, eg. 255.255.255.224
		~ CIDR (Classless Inter-Domain Routing) notation, eg. /27. It tells you how many bits in an IP address are used for the network portion​ (the rest are for hosts).
4. Devices can communicate directly if their IPs match the subnet (that means they are in the same network); If they are in different networks, they must go through a gateway(router) to commununicate.
5. All devices on the same cable/wireless must be in the same network.

	ATTENTION:
	IP Addresses & Subnet Masks Are Binary Numbers in Decimal Form:
	An IPv4 address​ (e.g., 192.168.1.1) is a 32-bit binary number split into 4 octets (8 bits each), displayed in decimal​ for readability.
	IP: 192.168.1.1 → 11000000.10101000.00000001.00000001
	
# default gateways

# swiches
1. In computer networking, a switch​ is a device that connects multiple devices (like computers, printers, or other switches/routers) on a local area network (LAN). Its primary job is to forward data packets​ to the correct destination based on the MAC address​ (Media Access Control address) of the receiving device.
2. HOW TO WORK:
   
4. 
# network loop
1. A network loop occurs when data packets circulate endlessly between network devices due to redundant paths and misconfigurations. This can cause boardcast storms (Uncontrolled flooding of traffic) and performance degradation (congestion and packet loss)

# OSI layers



