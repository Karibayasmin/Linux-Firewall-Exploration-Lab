# 🔥 Linux Firewall Exploration Lab

> A practical cybersecurity laboratory focused on configuring, testing, and analyzing Linux firewall behavior using **iptables**.

---

## 📖 Overview

This repository documents a hands-on firewall laboratory completed as part of my Master's studies in Cyber Security.

The objective was to understand how Linux firewalls inspect, filter, and control network traffic while implementing security rules using **iptables**.

Throughout the lab, different firewall configurations were created and evaluated to observe their impact on packet filtering, connection tracking, traffic limiting, and load balancing.

---

# This lab report documents the steps taken to configure firewall rules using iptables on a router to protect the router itself and the internal network. The tasks include setting up rules to prevent unauthorized access and ensuring proper network protection.

## 📸 Container setup: 


screenshots/firewall 1.png


## Checking for ipman, from the router 10.9.0.1 we can see that by default, ipman is not available in the container due to its minimal setup.  

```
screenshots/firewall 2.png
```

## After installing ipman 

```
screenshots/firewall 3.png
```

# Protecting the Router

## Set up rules to prevent outside machines from accessing the router machine, except for ping requests. Verify the configuration by attempting to ping and telnet into the router from an external machine.

## 📸 Commands Executed: 

```
screenshots/firewall 4.png
```

## Explanation of Commands: 

- **iptables -A INPUT -p icmp --icmp-type echo-request -j ACCEPT: Allows incoming ICMP echo-request packets (ping requests).** 
- **iptables -A OUTPUT -p icmp --icmp-type echo-reply -j ACCEPT: Allows outgoing ICMP echo-reply packets (ping responses).** 
- **iptables -P OUTPUT DROP: Sets the default policy for outgoing packets to DROP.** 
- **iptables -P INPUT DROP: Sets the default policy for incoming packets to DROP.**

## Observations

## Ping the Router 10.9.0.1 from 10.9.0.5: 

```
screenshots/firewall 5.png
``` 

## Explanation: The ping is successful because ICMP echo-request and echo-reply packets are allowed by the rules. 

## Telnet into the Router from 10.9.0.5: 

```
screenshots/firewall 6.png
``` 

## Explanation: The telnet connection is refused because the default INPUT and OUTPUT policies are set to DROP, and there are no specific rules to allow TCP traffic. 

Run the below clean-up commands before proceeding to the next task: 
- **iptables -F** 
- **iptables -P OUTPUT ACCEPT** 
- **iptables -P INPUT ACCEPT** 

---


## 👤 Author

**Kariba Yasmin**

🎓 M.Sc. in Cyber Security 

- *Former Android Software Engineer*

🔐 Interested in Network Security, Application Security, Security Engineering.

---

> *Security is not achieved by blocking everything. It is achieved by understanding what should be trusted.*
