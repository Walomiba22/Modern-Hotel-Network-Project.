# 🏨 Vic Modern Hotel: Enterprise Network Design

A comprehensive 3-story hotel network simulation featuring multi-layer segmentation, dynamic routing, and enterprise-grade security. Built and validated using **Cisco Packet Tracer**.

## 📍 Project Overview
The objective was to design a robust, scalable, and secure network for "Vic Modern Hotel." The architecture ensures that critical departments like Finance and Admin are isolated from public-facing services while maintaining seamless inter-departmental communication via OSPF.

## 🏗️ Network Architecture
The network is distributed across three logical tiers (floors):

*   **3rd Floor (Management):** Admin (VLAN 20), IT (VLAN 10), and the Core Server Room.
*   **2nd Floor (Corporate):** Finance (VLAN 50), HR (VLAN 40), and Sales (VLAN 30).
*   **1st Floor (Services):** Logistics (VLAN 60), Store (VLAN 70), and Reception (VLAN 80).

## 🚀 Key Technical Features
*   **Routing Protocol:** **OSPF (Area 0)** for dynamic routing and fast convergence across three Cisco 2911 routers.
*   **Inter-VLAN Routing:** Implemented via **Router-on-a-Stick** (802.1Q) to allow controlled communication between departments.
*   **Network Services:**
    *   **DHCP:** Centralized IP management for all endpoint devices (PCs, Printers, Laptops).
    *   **Wireless:** VLAN-integrated Access Points for mobile staff connectivity.
*   **Security Stack:**
    *   **SSH (v2):** RSA 2048-bit encrypted remote management.
    *   **Port Security:** "Sticky" MAC address filtering with `shutdown` violation mode on sensitive IT ports.

## 🔌 IP Addressing Plan


| Department | VLAN | Subnet | Gateway |
| :--- | :---: | :--- | :--- |
| IT Dept | 10 | 192.168.1.0/24 | 192.168.1.1 |
| Admin | 20 | 192.168.2.0/24 | 192.168.2.1 |
| Finance | 50 | 192.168.5.0/24 | 192.168.5.1 |
| Reception | 80 | 192.168.8.0/24 | 192.168.8.1 |

## 🛠️ How to Deploy
1.  Download and install **Cisco Packet Tracer** (v8.0 or higher).
2.  Clone this repository:
    ```bash
    git clone https://github.com
    ```
3.  Open the `.pkt` file located in the `/topology` folder.
4.  Run `show ip route` on any router to verify OSPF adjacency.

## 📊 Topology Diagram
![Network Topology](path/to/your/screenshot.png)

## 📜 License
This project is licensed under the MIT License.****
