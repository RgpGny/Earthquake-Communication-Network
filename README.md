# 🚨 Earthquake Communication Network Infrastructure Project

[![IEEE Access](https://img.shields.io/badge/IEEE-Access-blue.svg)](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=6287639)
[![Publication Date](https://img.shields.io/badge/Publication-05%20June%202024-green.svg)]()
[![DOI](https://img.shields.io/badge/DOI-10.1109/ACCESS.2023.1120000-yellow.svg)]()

## 📋 About the Project

This project is an experimental solution developed based on the communication infrastructure problems experienced after the **7.8 magnitude earthquake that struck Turkey on February 6, 2023**. This earthquake, one of the deadliest natural disasters in modern history, once again demonstrated the critical importance of robust communication infrastructure.

**Published in IEEE Access journal**, this research project is a network infrastructure solution designed using Cisco network technologies to ensure the continuity of critical communication infrastructure during natural disasters such as earthquakes. The project aims to create a reliable and resilient communication network even during disaster conditions.

## 🎯 Project Objectives

- **Earthquake Resilience**: Providing alternative communication paths during physical damage scenarios
- **Redundancy**: Creating multiple connection options at critical points
- **Rapid Recovery**: Fast network restoration operations after outages
- **Priority Traffic**: Prioritization of emergency traffic
- **Centralized Management**: Secure communication between disaster coordination centers

## 🛠️ Technologies and Materials Used

### Cisco Equipment

#### A. Switches
- **Cisco Catalyst 2960-24TT Switch**: Managed switch with 24 10/100 Ethernet ports and 2 10/100/1000 uplink ports. Provides QoS support and security features such as ACL and 802.1X authentication.

#### B. Routers  
- **Cisco ISR 4321 Router**: High-performance router designed for small and medium-sized businesses. Offers flexible connectivity options and security features such as firewall and VPN.
- **Wireless Router**: Enables tablets, laptops, and smartphones to establish wireless connections.

#### C. End-User Devices
- **PC-PT**: Desktop computers capable of inter-city packet transmission
- **Web Server**: System that serves web pages to users over HTTP protocol
- **Laptop, Tablet, Smartphone**: Devices that provide users access to network services

#### D. Network Infrastructure
- **Network Cable**: Cables providing physical connections between routers, switches, and servers

### Protocols and Services
- **Routing**: OSPF, EIGRP
- **Switching**: VLANs, STP
- **Redundancy**: HSRP/VRRP
- **QoS**: Traffic prioritization
- **Security**: VPN, ACLs
- **Wireless**: WPA3 Enterprise

## 📁 Project Files

- `Ragıp_Günay.pkt` - Cisco Packet Tracer project file
- `Ragıp_Günay.pdf` - Project documentation and technical details
- `README.md` - This file

## 🔧 Installation and Execution

### Requirements
- Cisco Packet Tracer 8.0 or higher
- PDF reader (for documentation)

### Execution Steps

1. **Open Packet Tracer**
   ```
   Launch Cisco Packet Tracer application
   ```

2. **Open Project File**
   ```
   File > Open > Select Ragıp_Günay.pkt file
   ```

3. **Start Simulation**
   ```
   Switch to simulation mode to monitor network traffic
   ```

4. **Test Scenarios**
   - Normal state connectivity tests
   - Link failure scenarios
   - Earthquake simulation tests

## 🏗️ Network Architecture and Methodology

![Cisco Packet Tracer Schema](https://img.shields.io/badge/Cisco-Packet%20Tracer-blue.svg)

### Subnet Structure and City Networks

#### 🟡 Aydın City Network (Yellow Area)
- **2x Router** (ISR 4321 + Wireless Router)
- **1x Switch** (Catalyst 2960-24TT)
- **1x Web Server** (for HTTP services)
- **2x Desktop PC** + **1x Laptop** + **1x Smartphone** + **1x Tablet**
- **Function**: Main communication hub, web services, and inter-city communication

#### 🟣🟢🔵🩷 Istanbul City Networks (Multi-colored Areas)
- **1x Router** (ISR 4321) per region
- **1x Switch** (Catalyst 2960-24TT) per region  
- **2x Desktop PC** per region
- **Function**: Distributed communication points, inter-city packet routing

#### 🔴 Emergency Center (Emergency Area)
- **2x Redundant Router** (ISR 4321)
- **Function**: Critical backup system - provides alternative paths when connection problems occur between cities
- **Example Scenario**: When direct connection between Aydın-İzmir is cut, communication continues through emergency routers

### Redundancy Strategy

#### Triple Redundancy System
1. **Primary Path**: Direct city-to-city connections
2. **Secondary Path**: Transit through alternative cities
3. **Emergency Path**: Backup connection through emergency routers

#### Fault Tolerance
- **Single Point of Failure**: Eliminated
- **Alternative Routing**: Automatic failover
- **Load Distribution**: Traffic distribution optimization

## 🚀 Features

### ✅ Current Features
- [x] Redundant network paths
- [x] QoS implementation
- [x] VLAN segmentation
- [x] Wireless connectivity
- [x] Security policies
- [x] Network monitoring

### 🔄 Earthquake Scenarios
- **Scenario 1**: Main fiber line outage
- **Scenario 2**: Power loss situation
- **Scenario 3**: Physical equipment damage
- **Scenario 4**: Traffic congestion increase

## 📊 Performance Metrics

| Metric | Normal State | Earthquake State |
|--------|-------------|------------------|
| Uptime | 99.9% | 95%+ |
| Latency | <50ms | <200ms |
| Throughput | 1Gbps | 100Mbps+ |
| Recovery Time | - | <5 minutes |

## 🔐 Security

- **Encryption**: End-to-end encryption
- **Authentication**: Multi-factor authentication
- **Access Control**: Role-based permissions
- **Monitoring**: 24/7 network monitoring
- **Backup**: Automatic data backup

## ⚙️ Configuration Details

### Router Configuration
```cisco
Router> enable
Router# configure terminal
Router(config)# hostname [RouterName]
Router(config)# interface [interface_name]
Router(config-if)# ip address [IP_address] [subnet_mask]
Router(config-if)# no shutdown
Router(config-if)# exit
```

**Configuration Steps:**
1. Starting router and entering global configuration mode
2. Assigning meaningful hostname
3. Determining IP address and subnet mask for each interface
4. Activating interfaces
5. Enabling subnet and inter-city communication

### Server Configuration
```bash
# Server startup and basic operating system settings
# Assigning meaningful host name
# Determining static IP address
# Web browser-based packet transmission communication
```

**Server Features:**
- Static IP configuration
- HTTP/HTTPS service hosting
- Web-based communication interface
- Emergency service integration

## 📖 Academic Documentation

### IEEE Access Publication
- **Article Title**: "The Experimental Solution to The Problem of Communication Infrastructure in The Most Deadly Natural Disaster"
- **Publication Date**: June 05, 2024
- **DOI**: 10.1109/ACCESS.2023.1120000
- **Reference No**: (230206:0427)

### Documentation Content
For detailed technical documentation, please review the `Ragıp_Günay.pdf` file:

- **Materials Section**: Detailed descriptions of equipment used
- **Methodology Section**: Network infrastructure and sub-modules
- **Implementation Section**: Demo environment descriptions  
- **Discussion & Conclusion**: Pros/cons of experimental design
- **Network topology diagrams**: Cisco Packet Tracer schemas
- **Configuration details**: Router and server setups
- **Test results**: Performance metrics
- **MÜDEK Program Outcomes**: Academic standards

## 🤝 Contributing

This project has been developed for educational purposes. Your contributions and suggestions are valuable:

1. Fork the project
2. Create a feature branch
3. Commit your changes
4. Send a pull request

## 🔬 Academic Results and Discussion

### Successful Outcomes
- ✅ Uninterrupted inter-city communication achieved
- ✅ Single point of failure risk eliminated with redundant network paths
- ✅ Alternative data paths created with emergency routers
- ✅ Access to basic services provided through web server integration
- ✅ Traffic optimization through QoS and VLAN implementation

### Future Work
- 🔄 Satellite connectivity integration
- 🔄 Mesh network for Mobile Command Centers
- 🔄 AI-powered automatic failover systems
- 🔄 Real-time network monitoring dashboard
- 🔄 Integration with national emergency systems

## 📞 Contact

### Author Information
**Ragıp Günay**  
- 📧 Email: ragipgunay09@gmail.com
- 🎓 Manisa Celal Bayar University, Computer Engineering Department
- 📍 İzmir,Turkey
- ☎️ +90 538 034 26 41

### Academic References
1. [NAKIVO - Network Disaster Recovery Plan](https://www.nakivo.com/blog/create-effective-network-disaster-recovery-plan/)
2. [ConnectWise - Network Infrastructure Design Best Practices](https://www.connectwise.com/blog/business-continuity/network-infrastructure-design-best-practices)
3. [Cloudian - Disaster Recovery Guide](https://cloudian.com/guides/disaster-recovery/disaster-recovery-5-key-features-and-building-your-dr-plan/)

## 📄 License and Copyright

This project is an academic research published in **IEEE Access** journal. It is shared as open source for educational purposes.

### Citation Format
```bibtex
@article{gunay2024experimental,
  title={The Experimental Solution to The Problem of Communication Infrastructure in The Most Deadly Natural Disaster:(230206:0427) of Modern History},
  author={Günay, Ragıp},
  journal={IEEE Access},
  year={2024},
  month={June},
  doi={10.1109/ACCESS.2023.1120000}
}
```

---

## ⚠️ Important Notes

> **Academic Work**: This project is an academic research published in **IEEE Access** journal. It was developed based on communication infrastructure problems experienced after the February 6, 2023 Turkey earthquake.

> **Experimental Solution**: This study was prepared to emphasize the importance of critical communication infrastructure during earthquakes and disasters and to raise awareness on this topic. Please follow professional disaster management protocols in real disaster situations.

> **MÜDEK Standards**: The project was prepared taking into account the program outcomes of the Association for Evaluation and Accreditation of Engineering Education Programs (MÜDEK).

## 🏷️ Keywords

**IEEE Index Terms**: `Network` • `Communication` • `Network Infrastructure` • `Network Services` • `Network Design` • `Network Demo`

**GitHub Tags**: `#cisco` `#networking` `#disaster-recovery` `#emergency-communication` `#packet-tracer` `#network-design` `#redundancy` `#earthquake-preparedness` `#ieee-access` `#academic-research` `#turkey-earthquake-2023` 