## **Network Simulation and VLAN Management**

### **Overview**
This project demonstrates the design and management of VLANs (Virtual Local Area Networks) in a simulated network environment using Cisco Packet Tracer. VLANs enhance network security and performance by segregating traffic based on roles or departments, with inter-VLAN routing enabling communication between VLANs.

### **Features**
- **VLAN Creation**:
  - Designed VLANs for various segments like IT, Finance, and Marketing to segregate traffic and reduce broadcast domains.
- **Inter-VLAN Routing**:
  - Configured routers and Layer 3 switches to facilitate controlled communication between VLANs.
- **Documentation**:
  - Detailed guides for configuring VLANs, assigning IP addresses, and enabling routing.

### **Tools & Technologies**
- **Cisco Packet Tracer**: Used to simulate network environments and test VLAN setups.

### **Installation & Setup**
#### **1. Obtain Cisco Packet Tracer**
- Download from [Cisco Networking Academy](https://www.netacad.com/).

#### **2. Open the Simulation File**
- Open the `.pkt` file included in this repository.

#### **3. Set Up VLANs**
- Example Configuration for Switch:
  ```bash
  enable
  configure terminal
  vlan 10
  name IT
  exit
  vlan 20
  name Finance
  exit
  interface fastEthernet 0/1
  switchport mode access
  switchport access vlan 10
  ```

#### **4. Enable Inter-VLAN Routing**
- Example Configuration for Router:
  ```bash
  enable
  configure terminal
  interface gigabitEthernet 0/0
  no shutdown
  ip address 192.168.10.1 255.255.255.0
  ```
  
### **Usage**
- **Traffic Simulation**:
  - Use Packet Tracer tools to simulate traffic between devices in different VLANs.
- **Network Testing**:
  - Test scenarios like bandwidth bottlenecks, unauthorized access attempts, and routing misconfigurations.
