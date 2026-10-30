# https-github.com-AravindP19-NETWORKWALKS-Aravind-Cybersecurity-Lab-Setup
Author: Aravind P GitHub: @AravindP19 Program: NETWORKWALKS Cybersecurity Internship,Week 1(WK1-PM1)
# Project Overview :
The purpose of this project is to setup a cybersecurity lab environment using VirtualBox environment and Kali Linux OS.

The goal is to create a controlled environment to learn cybersecurity concepts,testing with security tools and as a setup for future configurations.

The lab uses a dedicated NAT Network, allowing to configure Kali Linux with a constant IP address and setup the environment for additional virtual machines in future.

## Project Objectives:
The main objectives of the project are to:

1. Install and configure VirtualBox.

2. Import Kali Linux as a virtual machine.

3. Create a dedicated NAT Network.

4. Configure Kali Linux network connectivity.

5. Assign and verify the Kali VM's IP address.

6. Test Internet connectivity and DNS resolution.

7. Prepare a clean snapshot for future recovery.

8. Document the setup process and configuration.

## Architecture:

The lab runs Kali Linux in VirtualBox environment and connects to a dedicated NAT Network.

The network uses the 10.0.0.0/24 address range and the Kali VM uses the IP address 10.0.0.2/24.

Additional virtual machines can be connected to the same network in the future.

## Lab Configuration:
Component	Configuration
Host OS	Windows
Hypervisor	VirtualBox 7.2
Security OS	Kali Linux
Kali VM RAM	2048 MB
Virtual Network	NAT Network
Network Name	NatNetwork
Network Address	10.0.0.0/24
Kali IP Address	10.0.0.2/24
Default Gateway	10.0.0.1
Network Interface	eth0
<img width="235" height="352" alt="image" src="https://github.com/user-attachments/assets/ce692450-a83c-4ba0-a870-ada0ac2cd7a3" />

## Setup Procedure:
Step 1. Install 7-Zip
I installed 7-Zip to extract the Kali Linux virtual-machine archive.

Step 2. Install VirtualBox
I used VirtualBox as the hypervisor to create and manage my Kali Linux virtual machine.

Step 3. Create the NAT Network
I created a dedicated NAT Network in VirtualBox with the following configuration:

Network Name: NatNetwork

IPv4 Prefix: 10.0.0.0/24

DHCP: Enabled

IPv6: Disabled

This network configuration allows connected virtual machines to communicate with each other while providing outbound network connectivity.
## Application Screenshots

### 1. Architecture: 
![Architecture: Page](images/ss1.png)

### 2. Setup Procedure: 
![Setup Procedure: Page](images/ss2.png)

Step 4. Import Kali Linux
I downloaded Kali Linux from the official website and imported the virtual machine into VirtualBox.

The network adapter is configured as:

Attached to: NAT Network

Network: NatNetwork

The VM was allocated 2048 MB of RAM. 

Step 5. Configure the Kali Linux Network

I checked the Kali Linux network interface and verified its IP address.

The resulting configuration is:

IP Address: 10.0.0.2/24

Subnet Mask: 255.255.255.0

Default Gateway: 10.0.0.1

DNS: 10.0.0.1

## 4. Import Kali Linux: 
![Import Kali Linux: Page](images/ss3.png)

Step 6. Create a Clean VM Snapshot

After completing the initial configuration of my Kali Linux virtual machine, I created a VirtualBox snapshot to preserve the initial state of my lab.

This snapshot will serve as a recovery point for my virtual machine. If future experiments affect my configuration, I can restore the VM to its previous state with this.

Status: Completed — Snapshot creation and verification

# Lab Configuration Verification:

I used network commands to check my Kali Linux configuration and test internet connectivity. The following table summarizes my results and the additional checks pending:

|            Test            |            Command          |       Result / Status     |   |   |
|:-----------------------------:|:-----------------------------:|:---------------------------:|---|---|
| Check IP address           | ip a                          | Verified: 10.0.0.2/24       |   |   |
| Check routing table        | ip route                      | Verified: gateway 10.0.0.1  |   |   |
| Test Internet connectivity | ping google.com               | Successful replies received |   |   |
| Test gateway connectivity  | ping -c 4 10.0.0.1            | Not yet verified separately |   |   |
| Test DNS resolution        | nslookup networkwalks.com     | Not yet verified separately |   |   |
| Verify Nmap installation   | nmap --version                | Not yet verified            |   |   |
| Verify snapshot            | Restore snapshot and run ip a |    Completed                |   |   |

# Problems I faced and how I solved them:

Changing IPv4 settings can sometimes affect Internet connectivity so I set my DNS to IP 10.0.0.1 when I had issues with local DNS IP 8.8.8.8.

To check the network problems I checked the interface using ip a command,inspected the routing table with ip route command and tested connectivity using ping command.

# Learnings from this Lab:

By this project, I got a hands-on exposure to setting up an environment for practicing cybersecurity.
1. NAT vs. NAT Network
I learned that NAT and NAT Network serve different purposes. A NAT Network allows virtual machines connected to the same virtual network to communicate with one another while providing external network connectivity.

2. Virtual Machine Networking
I learned how VirtualBox network adapters connect my virtual machine to a virtual network and how the selected network mode affects communication and Internet access.

3. IP Addressing and Network Verification
I practiced checking my network interface, identifying my assigned IPv4 address, inspecting the routing table, and testing Internet connectivity from Kali Linux. I also learned that IP connectivity and DNS resolution are separate aspects of network troubleshooting.

5. VM Snapshots
I learned that snapshots provide recovery points for virtual machines. Creating a clean snapshot before experimenting with unfamiliar configurations can help me restore a known state if something goes wrong.

6. Technical Documentation
I learned the importance of documenting commands, configuration details, verification results, screenshots, and troubleshooting steps. Clear documentation makes my work easier to review and reproduce.

# Security Aspects and Ethical Usage:

I created this lab for educational purposes and for authorized cybersecurity practice. I will use it to develop my technical skills in a controlled environment and perform testing only on systems and networks for which I have permission.

# Tools and Resources:
7-Zip: https://7-zip.org/download.html

VirtualBox: https://virtualbox.org/wiki/Downloads

Kali Linux: https://kali.org/get-kali

# Author:
Aravind P

Aspiring Cybersecurity Professional

LinkedIn: linkedin.com/in/aravind-p-9614a51aa

# Project Details:
Program Name: Cybersecurity at NetworkWalks

Week: 01

Project: Cybersecurity & Pentesting Lab Setup

Repository: GitHub

