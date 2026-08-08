# Smart Server Room Monitoring Infrastructure

## 📝 Project Overview
This project demonstrates the design and configuration of a network infrastructure built to support a Smart Server Room Monitoring system. Designed in Cisco Packet Tracer, the lab establishes end-to-end connectivity across multiple routers and switches, integrating secure wireless access points for remote monitoring laptops and dedicated server nodes for data collection.

## 🎯 Objectives
* Design and deploy a multi-router network topology.
* Configure basic device security and interface IP addressing on Cisco routers (2911) and switches (2960).
* Implement secure wireless access (WPA2-PSK) for endpoint devices.
* Establish routing protocols to connect remote networks.
* Verify end-to-end connectivity between client devices and the central monitoring server.

## 🛠️ Technologies & Protocols
* **Simulation Tool:** Cisco Packet Tracer
* **Hardware:** Cisco 2911 Routers, Cisco 2960 Switches, Generic Access Points
* **Protocols:** IPv4, WPA2-PSK, ICMP, Static/Dynamic Routing

---

## 🗺️ Network Topology

[PLACE YOUR PICTURE HERE - Upload `image_ad529c.png` showing the full network map]

The network consists of two main sites connected via a serial/WAN link:
1. **Remote Access Site:** Features a laptop connected wirelessly to an Access Point, which connects to SW1 and R1.
2. **Data Center Site:** Features the main Server connected to SW2 and R2.

---

## 🚀 Implementation Steps

### Step 1: Base Device Configuration
Configured hostnames, basic security (enable secret passwords), and assigned IP addresses to the GigabitEthernet interfaces on both R1 and R2 to establish the foundational network structure.

[PLACE YOUR PICTURE HERE - Upload a cropped screenshot of the R1 Command Line showing the IP address configuration commands]

### Step 2: Wireless Network Setup
Configured the Home Router/Access Point (AP1) with a secure SSID and WPA2-PSK authentication to allow remote monitoring devices to securely join the network. 

[PLACE YOUR PICTURE HERE - Upload a screenshot of the AP1 Wireless GUI settings showing the SSID and password]

Successfully authenticated Laptop1 to the wireless network:

[PLACE YOUR PICTURE HERE - Upload a screenshot of Laptop1's "PC Wireless" module showing a successful connection]

### Step 3: Routing Configuration
Implemented routing between R1 and R2 to ensure the wireless subnet can communicate with the server subnet across the core link. 

[PLACE YOUR PICTURE HERE - Upload a screenshot of the `show ip route` command on R2 to prove the routing table is populated]

### Step 4: Server and IoT Services
Configured the central monitoring server (Server1) with a static IP address and enabled the necessary services to monitor the smart room environment.

[PLACE YOUR PICTURE HERE - Upload a screenshot of the "Services" tab on Server1 showing the IoT/Web services turned on]

---

## ✅ Verification and Testing
To ensure the infrastructure is fully operational, ICMP connectivity tests were performed from the edge device (Laptop1) across the routing boundary to the main server.

[PLACE YOUR PICTURE HERE - Upload a screenshot of Laptop1's Command Prompt showing a successful `ping` to Server1's IP address]

The successful replies confirm that routing, wireless authentication, and physical layer connections are properly established.
