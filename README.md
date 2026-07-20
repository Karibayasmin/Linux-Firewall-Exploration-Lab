# 🔥 Linux Firewall Exploration Lab

> A practical cybersecurity laboratory focused on configuring, testing, and analyzing Linux firewall behavior using **iptables**.

---

## 📖 Overview

This repository documents a hands-on firewall laboratory completed as part of my Master's studies in Cyber Security.

The objective was to understand how Linux firewalls inspect, filter, and control network traffic while implementing security rules using **iptables**.

Throughout the lab, different firewall configurations were created and evaluated to observe their impact on packet filtering, connection tracking, traffic limiting, and load balancing.

---

## 🎯 Objectives

The main objectives of this project were to:

- Understand Linux firewall architecture
- Configure packet filtering using iptables
- Explore Stateful and Stateless firewalls
- Implement Network Address Translation (NAT)
- Configure connection tracking (conntrack)
- Apply traffic rate limiting
- Implement load balancing using iptables
- Analyze firewall behavior through practical experiments

---

## 🛠 Technologies Used

- Linux
- iptables
- conntrack
- Netcat (nc)
- Ping
- Ubuntu Virtual Machines
- Virtual Network Environment

---

## 🔐 Topics Covered

✔ Packet Filtering

✔ Firewall Chains

✔ INPUT / OUTPUT / FORWARD Chains

✔ Stateful Firewall

✔ Stateless Firewall

✔ Network Address Translation (NAT)

✔ Connection Tracking

✔ ICMP Filtering

✔ Traffic Rate Limiting

✔ Firewall Rule Management

✔ UDP Load Balancing

---

## 🧪 Laboratory Tasks

### Task 1 — Basic Firewall Rules

Configured firewall rules to:

- Allow trusted traffic
- Drop unauthorized packets
- Verify communication using ping

---

### Task 2 — Stateful Firewall

Implemented connection tracking using **conntrack** to allow established and related connections while blocking unauthorized traffic.

Skills demonstrated:

- Stateful packet inspection
- Connection management
- Secure firewall configuration

---

### Task 3 — Rate Limiting

Configured ICMP rate limiting to reduce excessive ping requests and mitigate simple flooding attacks.

Implemented using:

- iptables
- limit module

---

### Task 4 — Network Address Translation (NAT)

Configured NAT rules to forward traffic between internal and external networks.

Concepts covered:

- Source NAT
- Destination NAT
- Packet forwarding

---

### Task 5 — Load Balancing

Implemented UDP load balancing using iptables.

Two techniques were explored:

- Round-Robin (nth mode)
- Random mode

Traffic was successfully distributed between multiple internal servers.

---

## 📈 Skills Demonstrated

- Linux Administration
- Firewall Configuration
- Network Security
- Packet Filtering
- Traffic Analysis
- Network Troubleshooting
- Access Control
- Security Rule Design
- Command Line Networking

---

## 📂 Repository Structure

```
screenshots/
        Network topology
        Firewall configuration
        Testing results

commands/
        iptables commands used
```

---

## 📚 Key Learning Outcomes

This project strengthened my understanding of:

- Linux networking fundamentals
- Firewall rule design
- Stateful packet inspection
- Network segmentation
- Traffic filtering strategies
- Practical cybersecurity troubleshooting
- Secure network architecture

---

## 👩‍💻 My Contribution

This laboratory was completed as part of a Master's Cyber Security course.

My contributions included:

- Firewall rule implementation
- Testing and validation
- Network traffic analysis
- Experiment documentation
- Result interpretation

---

## 🚀 Future Improvements

Planned future enhancements include:

- nftables implementation
- IPv6 firewall rules
- IDS/IPS integration (Snort/Suricata)
- Logging and monitoring
- Docker firewall configuration
- Cloud firewall implementation (AWS Security Groups)

---

## 👤 Author

**Kariba Yasmin**

🎓 M.Sc. Cyber Security

Former Android Software Engineer

🔐 Interested in Network Security, Application Security, Secure Software Development, and Cloud Security.

---

> *Security is not achieved by blocking everything. It is achieved by understanding what should be trusted.*
