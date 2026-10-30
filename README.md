# week1-Submission-kali-linux-lab-
Setting up a kali linux Lab environment for cybersecurity learning and practical exercises. This project covers kali linux installation, virtual machine configuration network setup and basic security testing in a controlled lab environment.
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ver-Virtualbox%20v7.2-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Linux-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Network-10.0.0.0%2F24-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Penetration%20Testing-C00000?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Virtualization-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Kali%20Linux-404040?style=flat-square&labelColor=C00000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/NetworkWalks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Waqas%20Karim%20CCIE-C00000?style=flat-square" />
</p>

## 📌 Project Overview
The Kali Linux Lab Setup project focuses on installing and configuring a Kali Linux environment for learning cybersecurity fundamentals and performing basic security testing in a controlled laboratory environment.

The project involves setting up Kali Linux using virtualization software such as VirtualBox or VMware, configuring basic network settings, exploring essential Linux commands, and understanding commonly used cybersecurity tools.

## 🎯 Objectives
To install and configure Kali Linux in a virtual machine environment.

To understand the basic features and functionality of the Kali Linux operating system.

To learn essential Linux commands and terminal operations.

To configure and understand basic network settings.

To explore commonly used cybersecurity tools for educational purposes.

To develop practical knowledge of cybersecurity fundamentals and ethical hacking.

To create a controlled lab environment for learning basic security testing.

To understand the importance of safe and authorized cybersecurity practices.

## 🛡️ Purpose of the Lab
The purpose of this lab is to create a safe and controlled environment for learning cybersecurity fundamentals using Kali Linux. It provides hands-on experience with Linux commands, network configuration, and basic security tools.

This lab helps develop practical skills in system administration, networking, and ethical hacking while understanding security vulnerabilities and preventive measures.

All experiments and security testing activities are performed only in authorized lab environments for educational purposes.

## 🏗️ Lab Architecture

![image alt](https://github.com/yogita-2213/week1-Submission-kali-linux-lab-/blob/cff956d8e4a7aff16bc1228c05bc858b71776b69/Screenshot%202026-10-30%20075453.png)

## ⚙️ Lab Configuration

| 🧩 Component       | ⚙️ Configuration   |
| ------------------ | ------------------  |
| 🖥️ Host OS         | Windows 10         |
| 🧠 Host RAM        | 8 GB               |
| ⚡ Processor       | Intel Core i7      |
| 🧰 Hypervisor      | VirtualBox 7.2  |
| 🐉 Security OS     | Kali Linux 2026.2  |
| 🧠 Kali RAM        | 2048 MB            |
| 🌐 Virtual Network | NAT Network        |
| 📡 Network Address | 10.0.0.0/24        |
| 🐧 Kali IP Address | 10.0.0.2/24        |
| 🚪 Default Gateway | 10.0.0.1           |
| 🌍 DNS Server      | 8.8.8.8            |
| 🔮 Future VM Range | 10.0.0.3–10.0.0.99 |

# 🪜 Lab Setup Procedure

## Step 1. Install 7-Zip

7-Zip was installed to extract the Kali Linux virtual-machine package, which may be distributed as a `.7z` archive.

**Tool:** 7-Zip

---

## Step 2. Install VirtualBox

VirtualBox was installed as the hypervisor.

---

## Step 3. Create the NAT Network
A dedicated NAT Network was created in VirtualBox.

Configuration:
Network Name: NatNetwork
IPv4 Prefix:  10.0.0.0/24
DHCP:         Enabled
IPv6:         Disabled

![image alt](https://github.com/yogita-2213/week1-Submission-kali-linux-lab-/blob/96ca2830ee2286e0b3548e7ce32a2653554c4615/Screenshot%202026-10-30%20081459.png)

A **NAT Network** was selected because multiple virtual machines connected to the same NAT Network can communicate with one another while also having outbound network connectivity.

This will allow future attacker and target VMs to communicate within the lab.


---

## Step 4. Import Kali Linux

The Kali Linux virtual machine was downloaded from the official Kali Linux website and imported into VirtualBox.

The VM network adapter was configured as follows:

```text
Adapter 1
Attached to: NAT Network
Network:     NatNetwork
Adapter Type: Intel PRO/1000 MT Desktop
...

The VM was allocated:

```text
RAM: 2048 MB
```
![image alt](https://github.com/yogita-2213/week1-Submission-kali-linux-lab-/blob/fa02daa00ddcf9bd47f0e08ee8f716a489941b2c/Screenshot%202026-10-30%20083033.png)
A shared folder was also configured for transferring required files between the host operating system and the Kali VM.



---

## Step 5. Configure the Kali Linux Network

The Kali Linux network configuration was checked and configured with a consistent IPv4 address.

Example configuration:

```text
IP Address: 10.0.0.2
Subnet Mask: 255.255.255.0
Gateway: 10.0.0.1
DNS: 8.8.8.8
```
A consistent IP address makes it easier to document the lab and reference the Kali machine in future exercises.

