<div align="center">

# Windows 10 Installation and Network Configuration in VirtualBox

**Installing and configuring Windows 10 in Oracle VirtualBox and integrating it with Kali Linux through a shared NAT Network.**

<p align="center">
  <img src="https://img.shields.io/badge/Project-Cybersecurity%20Lab-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/VirtualBox-v7.2-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Windows%2010-Operating%20System-0078D6?style=flat-square&labelColor=000000&logo=windows&logoColor=white" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Network-NAT%20Network-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/IPv4-10.0.0.0%2F24-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Focus-Network%20Configuration-C00000?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Technology-Virtualization-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Platform-GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Practice-Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Program-NetworkWalks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Mentor-Waqas%20Karim%20(CCIE)-C00000?style=flat-square" />
</p>

</div>

## 🪟 Windows 10 Lab Overview

This project focuses on installing and configuring **Windows 10 in Oracle VirtualBox** and integrating it with an existing **Kali Linux virtual machine** through a shared NAT Network.

The setup involves configuring static IPv4 addressing, establishing communication between both virtual machines, and verifying network and DNS connectivity. It provides a controlled environment for practicing network administration and authorized cybersecurity activities.

## 🎯 Lab Configuration Objectives

The main objectives of this lab  are to:

- Install and configure Windows 10 as a virtual machine in VirtualBox.
- Connect Windows 10 to the existing **NAT Network** used by Kali Linux.
- Configure static IPv4 addressing for the Windows 10 virtual machine.
- Establish network communication between Windows 10 and Kali Linux.
- Test internet connectivity from the Windows 10 virtual machine.
- Take a clean VM snapshot for recovery.
- Document the installation, network configuration, and testing procedures.
- Prepare the virtual environment for future networking and cybersecurity projects.

## 🔬 Lab Purpose and Virtualization Scope

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

## ⚙️ Virtualization Lab Environment Specifications

| 🧩 Component | ⚙️ Configuration |
|---|---|
| 🖥️ Host OS | Kali Linux 2026.3 |
| 🧠 Host RAM | 8 GB |
| ⚡ Processor | Intel Core i5 |
| 🧰 Virtualizaton Platform | VirtualBox 7.2.20 |
| 🐉 Existing VM | Kali Linux 2026.3 |
| 🧠 Kali RAM | 2048 MB |
| 🪟 Guest OS | Windows 10 |
| 🧠 Windows RAM | 3572 MB |
| 🌐 Virtual Network | NAT Network |
| 📡 Network Address | 10.0.0.0/24 |
| 🪟 Windows IP Address | 10.0.0.10/24 |
| 🚪 Default Gateway | 10.0.0.1 |
| 🌍 DNS Server | 8.8.8.8 |


## ⚙️ Windows 10 installation and network configuration steps 


### Step 1: Downloading Windows 10 ISO

Downloading the official Windows 10 ISO installation file from Microsoft. Selecting the appropriate system architecture (32-bit or 64-bit) based on the host computer's hardware compatibility and saving the ISO file for use during VirtualBox installation.

**Source:** [Microsoft](https://www.microsoft.com/software-download/windows10ISO)



### Step 2: Import and Configure Windows 10 Virtual Machine

Creating a Windows 10 VM in VirtualBox, allocating hardware resources, configuring virtual storage, and setting up a user account.

**Virtual Machine Specifications:**

```text
Operating System:       Windows 10 (64-bit)
Allocated RAM:          3572 MB
CPU Cores:              2
Video Memory:           128MB
Virtual Hard Disk:      40 GB 
Disk Allocation:        Dynamically Allocated
User Account:           Configured
Password:               Set during Windows setup
```
---

### Step 3: Windows 10 Installation and Initial Configuration

Starting the Windows 10 virtual machine and booting from the attached ISO file. Configuring the installation language, regional settings, and keyboard preferences. Accepting the license terms, selecting the virtual hard disk as the installation destination, and completing the Windows 10 installation.

**Installation Details:**

```text
Operating System:       Windows 10
Installation Media:     Windows 10 ISO
Installation Method:    Custom Installation
Installation Target:    40 GB Virtual Hard Disk
Virtualization Platform: Oracle VirtualBox 7.2
```


### Step 4: Configuring the VirtualBox Network Adapter

Accessing the Windows 10 virtual machine network settings in Oracle VirtualBox and configuring Adapter 1 to connect to the existing **NAT Network (NatNetwork)** shared with Kali Linux. Verifying the adapter configuration to establish communication between both virtual machines and provide internet connectivity.

**Network Adapter Configuration:**

```text
Adapter:       Adapter 1
Attached to:   NAT Network
Network:       NatNetwork
Adapter Type:  Intel PRO/1000 MT Desktop
```


### Step 5: Configuring Windows 10 Network Settings

Configuring the Windows 10 network adapter with a static IPv4 address and the required network parameters to establish communication with Kali Linux over the shared NAT Network.

Network Configuration:

```
IP Address:       10.0.0.10
Subnet Mask:      255.255.255.0
Default Gateway:  10.0.0.1
Preferred DNS:    8.8.8.8
```

Network Details:

- Network Type: VirtualBox NAT Network
- Network Address: `10.0.0.0/24`
- Kali Linux IP: `10.0.0.2`
- Windows 10 IP: `10.0.0.10`

Note: Ensure `10.0.0.10` is not assigned to another device or included in an active DHCP allocation.

---

### Step 6: Creating a Clean Windows 10 Snapshot

Creating a clean snapshot of the configured Windows 10 virtual machine in Oracle VirtualBox to preserve its current state for future restoration and cybersecurity lab activities.

**Snapshot Details:**

```text
Snapshot Name: Clean W10 - Network Setup
Status:       Successfully Created
```
### step 7: 🔎 Network Connectivity Verification

Performing network tests to verify successful communication between the Windows 10 and Kali Linux virtual machines, gateway accessibility, internet connectivity, and DNS resolution.

| ✅ Test | 🧾 Command | 🎯 Expected Result |
|---|---|---|
| 🌐 Check IP configuration | `ipconfig` | Correct Windows 10 IP address displayed |
| 🐉 Test Kali Linux connectivity | `ping 10.0.0.2` | Successful replies from Kali Linux |
| 📡 Test gateway connectivity | `ping 10.0.0.1` | Successful replies from gateway |
| 🌍 Test Internet connectivity | `ping 8.8.8.8` | Successful replies from Google DNS |
| 🔎 Verify DNS resolution | `nslookup networkwalks.com` | Successful domain name resolution |
| 🔄 Verify snapshot | Restore snapshot | Baseline configuration restored |

**Verification Result:** Successfully establishing network communication between Windows 10 and Kali Linux and confirming DNS resolution.


