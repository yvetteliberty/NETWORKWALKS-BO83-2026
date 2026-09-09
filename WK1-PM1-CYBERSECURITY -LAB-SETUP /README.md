# 🛡️Cybersecurity Lab Environment Setup
### This is an isolated Virtual Lab Build for Penetration  Testing  and Ethical Hacking Practice From Intership.
![Skill](https://img.shields.io/badge/Skill-Cybersecurity-00b894?style=flat-square)

![Network](https://img.shields.io/badge/Network-10.0.0.0%2F24-green?style=flat-square)
![Penetration](https://img.shields.io/badge/Penetration-Testing-red?style=flat-square)
![VirtualBox](https://img.shields.io/badge/VirtualBox-v7.2-blue?style=flat-square)
![Kali Linux](https://img.shields.io/badge/Kali--Linux-v2026.2-5579c6?style=flat-square)
![Ethical Hacking](https://img.shields.io/badge/Ethical%20Hacking-Yvette%20Ngozi-e74c3c?style=flat-square)
<hr>

# 🎯Project Overview
This project involves building a virtual cybersecurity and penetration-testing lab using VirtualBox and Kali Linux.

The lab provides a secure and isolated environment for practicing cybersecurity techniques, including network reconnaissance, scanning, vulnerability assessment, and security testing. It is designed to support hands-on learning while allowing testing activities to be conducted safely without affecting production systems.

The environment uses a private virtual network, making it possible to add additional virtual machines as authorized targets for testing. This setup provides a flexible and repeatable platform for developing practical cybersecurity and ethical-hacking skills.

<hr>

# 📌Purpose 
The main Purpose of this project is to:

- Install and configure VirtualBox.
- Install/import Kali Linux as a virtual machine.
- Create a private NAT Network for the cybersecurity lab.
- Configure network connectivity for Kali Linux.
- Assign a consistent IP address to the Kali VM.
- Verify network connectivity and DNS resolution.
- Take a clean VM snapshot for recovery.
- Document the complete setup process.
- Prepare the environment for future cybersecurity projects.
<hr>

# 🛡️ Goal
The Goal is to create an Isolated environment for Hand-on Practise for the Cybersecurity Leaning on an authorized security environment.
It will be used for Penetration and Ethical hacking  cybersecurity activities, which includes:

- Network reconnaissance
- Port scan
- Vulnerability assessment
- Packet analysis
- Web application security testing
- Exploitation and penetration-testing practice
- Experimentation with security tools
  
<hr>

  # 🔍Lab Architecture

  <img width="830" height="371" alt="image" src="https://github.com/user-attachments/assets/4509da00-5927-456f-90fc-c1869e0d7285" />
 <hr>
 
 # ⚙️ Lab Configuration

 ## 🖥️ Lab Environment Configuration

| 🧩 Component | ⚙️ Configuration |
 |---|---|
| 🧠 Host RAM | 16 GB |
| ⚡ Processor | Intel Core i5 |
| 🧰 Hypervisor | VirtualBox 7.2 |
| 🐉 Security OS | Kali Linux 2026.2 |
| 🧠 Kali RAM | 2048 MB |
| 🌐 Virtual Network | NAT Network |
| 📡 Network Address | 10.0.0.0/24 |
| 🐧 Kali IP Address | 10.0.0.3/24 |
| 🚪 Default Gateway | 10.0.0.1 |
| 🌍 DNS Server | 8.8.8.8 |

<hr>

# 🧰 Tools Used: 
The following Tools were used on this Project and there are as follows:
- Laptop
- Virtual Box
- Kali Linux
- 7.zip
<hr>

# ⏳ Procedures

# Step 1. 
Install  7.zip : This tool is use to extract kali inux from machine package.

# Step 2. 
Install Virtual box : 
A free, open-source program that  run multiple operating systems (like Windows, Linux, or macOS) at the same time on a single computer.

# Step 3. 
Configure Network on The Virtual Box.
NAT network was set on the Virtual Box  with an IP address of 10.0.0.0/24,and Name :NAT Network 2 with DHCP Sever Enabled 
<img width="948" height="445" alt="image" src="https://github.com/user-attachments/assets/0505fb87-bd85-40b9-b38d-41a3937e3088" />

 NAT Network was selected because multiple virtual machines connect to the same NAT Network can communicate with one another while also having outbound network connectivity.
This allows intraction between the attacker and the Target Mechine to communicate within the lab.

#  Step 4.
Import Kali Linux 
The kali linux was downloaded from the official kali site and was imported into the virtual box.The VM allocated RAM is 2048 MB
<img width="899" height="419" alt="image" src="https://github.com/user-attachments/assets/d0fe4840-2687-49ee-9993-cad8b2646e98" />
<img width="905" height="427" alt="image" src="https://github.com/user-attachments/assets/8fc4c295-60d7-4475-b893-46d06ad61918" />

# Step 5.
Set Up IP configuration On Kali Linux
The Kali linux network was configured with an IP address of 10.0.0.3 ,netmask :255.255.255.0 and default getway : 10.0.0.1,DNS 8.8.8.8

<img width="353" height="272" alt="image" src="https://github.com/user-attachments/assets/3eae13a1-a2ea-462a-8ca4-cffc4ace0f7b" />

# Step 6
Take snapshot of the VM
After the configuration of the kali linux,a snapshot was taken to document the clean state of the kali linux .

# 🔍 Lab Verification
 
