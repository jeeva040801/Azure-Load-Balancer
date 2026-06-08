# Azure Load Balancer High Availability

## Project Overview

This project demonstrates how Azure Load Balancer distributes incoming traffic across multiple virtual machines to provide high availability and fault tolerance.

A highly available web application environment was created using two Linux virtual machines hosting separate web pages. Azure Load Balancer was configured to route incoming traffic to healthy backend instances.

## Architecture

```text
                Internet
                    │
                    ▼
            Azure Load Balancer
                    │
        ┌───────────┴───────────┐
        ▼                       ▼
     WebVM1                  WebVM2
  (Apache/Nginx)         (Apache/Nginx)
```

                                                                     

---

## Business Scenario

Organizations hosting web applications need to ensure uninterrupted service availability. If a single server fails, users should still be able to access the application without downtime.

Azure Load Balancer provides:

* Traffic distribution
* High availability
* Fault tolerance
* Improved application reliability

---

## Architecture

Client Browser
↓
Azure Public Load Balancer
↓
Backend Pool
├── Web Server 1 (Apache/Nginx)
└── Web Server 2 (Apache/Nginx)

---

## Technologies Used

* Microsoft Azure
* Azure Virtual Machines
* Azure Virtual Network
* Azure Load Balancer
* Linux (Ubuntu)
* Apache/Nginx Web Server

---

## Implementation Steps

1. Created a Virtual Network and Subnet.
2. Provisioned two Ubuntu Virtual Machines.
3. Installed web server software on both VMs.
4. Created unique index.html pages on each server.
5. Configured Azure Load Balancer.
6. Added VMs to the backend pool.
7. Configured health probes and load balancing rules.
8. Tested traffic distribution through the Load Balancer Public IP.

---

## Validation

* Verified successful access through Load Balancer Public IP.
* Refreshed browser multiple times to observe traffic distribution.
* Confirmed service availability when backend instances were healthy.

---

## Key Learnings

* Azure Load Balancer architecture
* Backend pools and health probes
* Layer 4 traffic distribution
* High availability design patterns
* Azure networking fundamentals

---

## Skills Demonstrated

* Azure Networking
* Virtual Machines
* Load Balancer Configuration
* High Availability
* Infrastructure Management
* Cloud Administration

---

## Screenshots

* architecture.png
* vm-list.png
* web-server-1.png
* web-server-2.png
* health-probe.png
* load-balancing-rule.png
* health-status.png
* server1-response.png
* server2-response.png

---

## Outcome

Successfully deployed a highly available web application environment using Azure Load Balancer and multiple backend virtual machines, demonstrating traffic distribution and fault-tolerant infrastructure design.
