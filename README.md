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



