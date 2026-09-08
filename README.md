# CYBERSECURITY-ENVIRONMENT-LAB-SET-UP
# MY WEEK 1 PROJECT AT NETWORK WALKS
Building an isolated virtual lab for penetration testing and ethical hacking practice

![Cybersecurity](https://img.shields.io/badge/Skill-Cybersecurity-red)
![VirtualBox](https://img.shields.io/badge/Ver-VirtualBox%20v7.2-blue)
![Kali Linux](https://img.shields.io/badge/Kali%20Linux-v2026.2-black)
![Linux](https://img.shields.io/badge/Skill-Linux-orange)
![Networking](https://img.shields.io/badge/Network-10.0.0.0%2F24-green)
![Penetration Testing](https://img.shields.io/badge/Penetration%20Testing-Expert-red)
![Virtualization](https://img.shields.io/badge/Skill-Virtualization-purple)
![GitHub](https://img.shields.io/badge/GitHub-Projects-black)
![Ethical Hacking](https://img.shields.io/badge/Ethical%20Hacking-Practical-red)
![NetworkWalks](https://img.shields.io/badge/NetworkWalks-Networking-blue)
![ATEMLEFAC NKAFU BECHEM](https://img.shields.io/badge/ATEMLEFAC%20NKAFU%20BECHEM-Cybersecurity-black)

# PROJECT OVERVIEW
This project focuses on building a virtual cybersecurity and penetration-testing laboratory using VirtualBox and Kali Linux. The lab provides a controlled and isolated environment for practicing network reconnaissance, scanning, vulnerability assessment, ethical hacking, and security testing in a safe and repeatable manner. The environment is configured using a 10.0.0.0/24 NAT Network, with Kali Linux serving as the primary security-testing machine. The lab is designed to support the addition of other virtual machines as targets for authorized penetration-testing exercises, network security assessments, and future CTF challenges.

# 🎯 OBJECTIVES
The main objectives of this project are to:
- Build a virtual cybersecurity and ethical-hacking testing environment.
- Install and configure Kali Linux as the primary penetration-testing machine.
- Configure a 10.0.0.0/24 NAT Network for virtual machine communication.
- Configure Kali Linux with a 10.0.0.2/24 IP address and Internet access.
- Enable secure file sharing, clipboard, and drag-and-drop between host and VM.
- Verify network connectivity and DNS resolution.
- Create VM snapshots for recovery and repeatable testing.
- Prepare the environment for additional Windows/Android target machines.
- Establish a practical lab for penetration testing, cybersecurity exercises, and CTF challenges.

 # 🎯 Purpose of the Lab

The lab provides an **isolated and controlled environment for cybersecurity 
learning, ethical-hacking practice, and authorized security testing**.

It can be used for:

- Network reconnaissance
- Network and port scanning
- Vulnerability assessment
- Network security testing
- Penetration-testing practice
- Security-tool experimentation
- Multi-VM security testing
- CTF and practical cybersecurity challenges

The environment can also be extended with additional virtual machines to 
provide controlled targets for authorized security-testing exercises. 

# 🏗️ Lab Architecture
<img width="1346" height="616" alt="image" src="https://github.com/user-attachments/assets/691854da-9d65-4038-817e-a11f22df2101" />
Additional target machines can be added to the same virtual network in future projects.

# ⚙️ Lab Configuration
🧩 Component             	⚙️ Configuration
- 🖥️ Host OS            - Windows 10
- 🧠 Host RAM	           - 8 GB
- ⚡ Processor          	- Intel Core i7
- 🧰 Hypervisor    	    - VirtualBox 7.2
- 🐉 Security OS	        - Kali Linux 2026.2
- 🧠 Kali RAM    	       - 2048 MB
- 🌐 Virtual Network    	- NAT Network
- 📡 Network Address	    - 10.0.0.0/24
- 🐧 Kali IP Address    	- 10.0.0.2/24
- 🚪 Default Gateway    	- 10.0.0.1
- 🌍 DNS Server          - 	8.8.8.8
- 🔮 Future VM Range	    - 10.0.0.3–10.0.0.99

# Lab Setup Procedures
# Step 1. Download and Install 7-Zip
<img width="1206" height="623" alt="DOWNLOADING 7-ZIP" src="https://github.com/user-attachments/assets/568c2c52-8e73-4643-8c86-750e2bae92b3" />

7-Zip was installed to extract the Kali Linux virtual-machine package, which may be distributed as a .7z archive.

Tool: 7-Zip

# Step 2. Download and Install VirtualBox
<img width="1523" height="708" alt="DOWNLOADING VIRTUAL BOX" src="https://github.com/user-attachments/assets/d1709c37-ce9d-435e-8cf7-15a7048af4db" />

<img width="528" height="399" alt="INSTALLING VIRTUAL BOX" src="https://github.com/user-attachments/assets/b6ecd55a-6e3b-4417-b2a9-f54e29aeda7f" />

VirtualBox was installed as the hypervisor.

# Step 3. Create the NAT Network
A dedicated NatNetwork was configured using the 10.0.0.0/24 IPv4 subnet, with DHCP enabled for automatic IP assignment and IPv6 disabled.
<img width="1585" height="817" alt="CONFIGURING NAT NETWORKS" src="https://github.com/user-attachments/assets/a10245da-4313-4a46-bfa2-343d3511eea2" />
A NAT Network was chosen to enable communication between multiple virtual machines within the same isolated network while still providing outbound internet connectivity.

This configuration will allow future attacker and target VMs to communicate effectively within the cybersecurity lab environment.

# Step 4. Import Kali Linux
The Kali Linux virtual machine was obtained from the official Kali Linux website and subsequently imported into VirtualBox.

The VM’s network adapter was then configured with the following settings:
Adapter 1
Attached to: NAT Network
Network:     NatNetwork
Adapter Type: Intel PRO/1000 MT Desktop

The VM was allocated:
# RAM: 2048 MB
<img width="1598" height="841" alt="OPENING KALI ON VIRTUAL BOX" src="https://github.com/user-attachments/assets/224e403c-bdd7-4fda-97a4-3a9f88ad236d" />

<img width="1600" height="828" alt="KALI LINUX INTERFACE" src="https://github.com/user-attachments/assets/e74a23c0-bdce-4354-999a-17bb27d743c1" />
This is how the kali Linux interface looks like

# Step 5. Configure the Kali Linux Network
The Kali Linux network configuration was checked and configured with a consistent IPv4 address.

Example configuration:
IP Address: 10.0.0.2
Subnet Mask: 255.255.255.0
Gateway: 10.0.0.1
DNS: 8.8.8.8

<img width="835" height="560" alt="SETTING UP WIRED CONNECTION" src="https://github.com/user-attachments/assets/387da871-151a-4ef5-980e-c1c979a10d8d" />

# Step 6. Create a Clean VM Snapshot
After completing the initial configuration, a VirtualBox snapshot was created.

Example snapshot name:
# My kali Linux after installation

The snapshot represents the clean baseline of the laboratory.

If a future exercise changes or damages the VM configuration, the machine can be restored to this baseline.
