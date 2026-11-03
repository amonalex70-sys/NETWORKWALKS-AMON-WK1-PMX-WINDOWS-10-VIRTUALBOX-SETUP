<div align = "center">

# 🖥️ Windows 10 virtualbox Installation and  Network Configuration

<div align = "center"> 
  
**installation and network configuration in combination with Kali Linux via a shared NAT network.**

<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ver-VirtualBox%20v7.2-0070C0?style=flat-square&labelColor=000000&logo=virtualbox&logoColor=white" />
  <img src="https://img.shields.io/badge/OS-Windows%2010-0078D6?style=flat-square&labelColor=000000&logo=windows&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Windows%20Administration-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Network-10.0.0.0%2F24-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Virtualization-VirtualBox-404040?style=flat-square&labelColor=0070C0" />
  <img src="https://img.shields.io/badge/Skill-Networking-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Windows%2010-404040?style=flat-square&labelColor=0078D6&logo=windows&logoColor=white" />
  <img src="https://img.shields.io/badge/NetworkWalks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/NAT%20Network-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Waqas%20Karim%20CCIE-C00000?style=flat-square" />
  
</p>

</div>
</div>


## 📌 Project Overview

This project focuses on the installation, configuration, and integration of **Windows 10 as a virtual machine within Oracle VirtualBox** as part of a practical cybersecurity lab environment.

The Windows 10 virtual machine is configured to operate on an existing **VirtualBox NAT Network**, shared with Kali Linux, to establish communication between the two operating systems. The project also involves configuring network settings, assigning a static IPv4 address, and performing connectivity tests to verify communication, gateway accessibility, and internet access.

This setup provides a controlled virtual environment for exploring Windows and Linux networking, system administration, and practical cybersecurity activities.

## 🎯 Objectives

The main objectives of this project are to:

- Install and configure Windows 10 as a virtual machine in VirtualBox.
- Connect Windows 10 to the existing **NAT Network** used by Kali Linux.
- Configure static IPv4 addressing for the Windows 10 virtual machine.
- Establish network communication between Windows 10 and Kali Linux.
- Test internet connectivity from the Windows 10 virtual machine.
- Take a clean VM snapshot for recovery.
- Document the installation, network configuration, and testing procedures.
- Prepare the virtual environment for future networking and cybersecurity projects.

## 🛡️ Purpose of the Lab

The purpose of this lab is to establish an isolated and controlled virtual environment for cybersecurity learning, network administration, and authorized security testing.

By integrating Windows 10 with Kali Linux through a shared NAT Network, the lab provides a practical environment for:

- Network communication and reconnaissance.
- Port scanning and service identification.
- Vulnerability assessment.
- Network traffic and packet analysis.
- Windows security configuration and testing.
- Security-tool experimentation.
- Practical penetration testing in an authorized environment.

⚠️ **Important:** This laboratory must only be used for systems that you own or have explicit permission to test. Do not use the lab or its tools to attack unauthorized systems.

## ⚙️ Lab Configuration

| 🧩 Component | ⚙️ Configuration |
|---|---|
| 🖥️ Host OS | Kali Linux 2026.3 |
| 🧠 Host RAM | 8 GB |
| ⚡ Processor | Intel Core i5 |
| 🧰 Virtualization | VirtualBox 7.2.20 |
| 🪟 Guest OS | Windows 10 |
| 🧠 Windows RAM | 2048 MB |
| 🐉 Existing VM | Kali Linux 2026.3 |
| 🧠 Kali RAM | 2048 MB |
| 🌐 Virtual Network | NAT Network |
| 📡 Network Address | 10.0.0.0/24 |
| 🐧 Kali IP Address | 10.0.0.2/24 |
| 🪟 Windows IP Address | 10.0.0.10/24 |
| 🚪 Default Gateway | 10.0.0.1 |
| 🌍 DNS Server | 8.8.8.8 |
| 🔮 Future VM Range | 10.0.0.3–10.0.0.99 |

# ⚙️ Windows 10 Installation and Configuration Procedure

### Step 1: Download Windows 10 ISO

- Download the official Windows 10 ISO from [Microsoft](https://www.microsoft.com/software-download/windows10ISO).
- Select the 64-bit (x64) version.
- Save the ISO file for use during VirtualBox installation.
