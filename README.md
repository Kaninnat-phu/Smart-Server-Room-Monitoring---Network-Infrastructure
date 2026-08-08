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

<img width="1467" height="846" alt="topology" src="https://github.com/user-attachments/assets/4cd3c1b8-6ec2-44af-abe0-965321f023dc" />

The network consists of two main sites connected via a serial/WAN link:
1. **Remote Access Site:** Features a laptop connected wirelessly to an Access Point, which connects to SW1 and R1.
2. **Data Center Site:** Features the main Server connected to SW2 and R2.

---

## 🚀 Implementation Steps

### Step 1: Base Device Configuration
Configured hostnames, basic security (enable secret passwords), and assigned IP addresses to the GigabitEthernet interfaces on both R1 and R2 to establish the foundational network structure.

<img width="694" height="694" alt="image" src="https://github.com/user-attachments/assets/931aba6f-d523-4074-9ebc-00c3cd824cbe" />

### Step 2: Wireless Network Setup
Configured the Home Router/Access Point (AP1) with a secure SSID and WPA2-PSK authentication to allow remote monitoring devices to securely join the network. 

<img width="886" height="679" alt="image" src="https://github.com/user-attachments/assets/746d40b4-162a-46e2-a7eb-5698893dd562" />


Successfully authenticated Laptop1 to the wireless network:

<img width="687" height="681" alt="image" src="https://github.com/user-attachments/assets/b5ed2a28-9091-4aca-b35e-989a8f650192" />

### Step 3: Routing Configuration
Implemented routing between R1 and R2 to ensure the wireless subnet can communicate with the server subnet across the core link. 

<img width="688" height="643" alt="image" src="https://github.com/user-attachments/assets/f09b3d17-9f34-46db-b9b5-e67e24009048" />


### Step 4: Server and IoT Services
Configured the central monitoring server (Server1) with a static IP address and enabled the necessary services to monitor the smart room environment.

<img width="691" height="675" alt="image" src="https://github.com/user-attachments/assets/a1a2364a-2839-4f57-95bc-9bb54896c416" />


---

## ✅ Verification and Testing
To ensure the infrastructure is fully operational, ICMP connectivity tests were performed from the edge device (Laptop1) across the routing boundary to the main server.

<img width="334" height="163" alt="image" src="https://github.com/user-attachments/assets/6fcce37b-a893-4c30-ad5f-555774272291" />

The successful replies confirm that routing, wireless authentication, and physical layer connections are properly established.

## 📁 Repository Structure

```text
├── images/                   # Folder containing all screenshots
│   ├── topology.png
│   ├── r1_config.png
│   ├── wireless_setup.png
│   └── ping_test.png
├── configs/                  # (Optional) Text files of your router/switch configs
│   ├── R1_run_config.txt
│   └── R2_run_config.txt
├── smart_server_room.pkt     # The actual Cisco Packet Tracer project file
└── README.md                 # This documentation file

