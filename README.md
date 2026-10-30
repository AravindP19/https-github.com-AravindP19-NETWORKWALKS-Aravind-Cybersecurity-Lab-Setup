# https-github.com-AravindP19-NETWORKWALKS-Aravind-Cybersecurity-Lab-Setup
Author: Aravind P GitHub: @AravindP19 Program: NETWORKWALKS Cybersecurity Internship,Week 1(WK1-PM1)
# Project Overview :
This project is to setup a cybersecurity lab environment using VirtualBox and Kali Linux.

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

## 3. Import Kali Linux: 
![Import Kali Linux: Page](images/ss3.png)

Step 6. Create a Clean VM Snapshot

After completing the initial configuration of my Kali Linux virtual machine, I created a VirtualBox snapshot to preserve the initial state of my lab.

This snapshot will serve as a recovery point for my virtual machine. If future experiments affect my configuration, I can restore the VM to its previous state with this.

Status: Completed — Snapshot creation and verification


