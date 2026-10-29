# 🔐 Cybersecurity Lab Environment Setup

**Building an isolated virtual lab for cybersecurity learning and penetration-testing practice.**

![Cybersecurity](https://img.shields.io/badge/Skill-Cybersecurity-red)
![VirtualBox](https://img.shields.io/badge/VirtualBox-Virtualization-blue)
![Kali Linux](https://img.shields.io/badge/OS-Kali%20Linux-blue)
![Networkwalks](https://img.shields.io/badge/Program-Networkwalks-orange)

---

## 📌 Project Overview

This project focuses on setting up a virtual cybersecurity and penetration-testing laboratory using Oracle VirtualBox and Kali Linux on my Windows 11 laptop.

The purpose of this lab is to create a controlled environment for learning cybersecurity tools, network scanning, reconnaissance, vulnerability assessment, and other security-testing activities.

During this hands-on project, I explored virtual machine settings, network configuration, IP address inspection, and basic connectivity verification.

This project is part of the **Networkwalks Cybersecurity Program — Batch B082, Week 1**.

---

## 🎯 Objectives

The main objectives of this project are to:

* Install and configure Oracle VirtualBox.
* Configure Kali Linux as a virtual machine.
* Create a virtual network named `Cyberlab`.
* Inspect network settings and assigned IP addresses.
* Understand basic network connectivity verification.
* Create a virtual machine snapshot for recovery.
* Document the complete setup process.
* Prepare the environment for future cybersecurity projects.

---

## 🛡️ Purpose of the Lab

The lab provides a controlled environment for cybersecurity learning and authorized security testing.

It can be used for activities such as:

* Network reconnaissance
* Port scanning
* Vulnerability assessment
* Network troubleshooting
* Web application security testing
* Penetration-testing fundamentals

**⚠️ Ethical Use:** This laboratory is intended for educational purposes and authorized security testing only. Do not use the lab or its tools to attack systems without permission.

---

## 🏗️ Lab Architecture
<img width="1346" height="616" alt="WhatsApp Image 2026-10-29 at 10 48 22 PM" src="https://github.com/user-attachments/assets/c53eeba0-a8be-4277-adde-8c37c849cd43" />


The laboratory uses Windows 11 as the host operating system, Oracle VirtualBox as the hypervisor, and Kali Linux as the guest operating system.

Kali Linux runs inside VirtualBox and connects to the configured `Cyberlab` virtual network.

Additional virtual machines can be added to the virtual network in future projects, depending on the network configuration and lab requirements.

---

## ⚙️ Lab Configuration

| 🧩 Component                | ⚙️ Configuration  |
| --------------------------- | ----------------- |
| 💻 Host OS                  | Windows 11        |
| 🖥️ Hypervisor              | Oracle VirtualBox |
| 🐉 Security OS              | Kali Linux        |
| 🌐 Virtual Network          | `Cyberlab`        |
| 🔌 Network Type             | NAT Network       |
| 📡 Observed Network Subnet  | `10.0.2.0/24`     |
| 🐧 Observed Kali IP Address | `10.0.2.3`        |

**Configuration Note:** The subnet and IP address shown above reflect the values observed in my environment. Other settings should be added only after checking the actual configuration.

---

## 🪜 Lab Setup Procedure

### Step 1. Prepare the Virtualization Environment

Oracle VirtualBox was used to run Kali Linux inside a virtual machine on my Windows 11 laptop.

This allowed me to work with a Linux environment without replacing my host operating system.

**Tool:** Oracle VirtualBox

### Step 2. Configure Kali Linux

Kali Linux was configured as the guest operating system inside VirtualBox.

I explored the virtual machine settings and became familiar with the configuration required to run the cybersecurity environment.

**Tool:** Kali Linux

### Step 3. Create the NAT Network
<img width="1600" height="900" alt="WhatsApp Image 2026-10-29 at 9 53 59 PM" src="https://github.com/user-attachments/assets/7a5ccf24-c3ba-4eb4-96d8-eb79fb30bbdc" />


A virtual network named `Cyberlab` was created in VirtualBox.

I explored the network settings to understand how a virtual machine connects to the configured network.

**Network Name:** `Cyberlab`

**Network Type:** NAT Network

### Step 4. Connect Kali Linux to the Network

I checked the network adapter settings assigned to the Kali Linux virtual machine.

During this process, I identified a network connection named `Wired connection 1` inside Kali Linux.

This helped me understand the relationship between the virtual network configured in VirtualBox and the network connection visible inside the guest operating system.

### Step 5. Inspect the IP Address

I used the following command to inspect the IP address assigned to Kali Linux.

```bash
ip a
```

The command displayed the available network interfaces and their assigned IP addresses.

My environment showed `10.0.2.3`, while the instructor's sample project used `10.0.0.2`.

I learned that IP addresses depend on the network configuration and that sample values should not be copied without checking the actual environment.

### Step 6. Verify Network Connectivity

I checked the network configuration and used connectivity checks to understand how to test communication with another destination.

I also opened a website in the Kali Linux browser to check browser-based internet access.

I learned that checking an IP address, testing connectivity, verifying DNS resolution, and opening a website are separate verification activities.

### Step 7. Create a Virtual Machine Snapshot

I created a VirtualBox snapshot to preserve a recovery point for future lab activities.

A snapshot can help restore a previously saved virtual machine state if later experiments change the system configuration.

---

## 🔎 Lab Verification

| 🔍 Check         | 🛠️ Command / Method        | 🎯 Purpose                                  |
| ---------------- | --------------------------- | ------------------------------------------- |
| IP configuration | `ip a`                      | Inspect network interfaces and IP addresses |
| Connectivity     | `ping <destination-IP>`     | Test communication with a destination       |
| DNS resolution   | `nslookup networkwalks.com` | Check domain name resolution                |
| Browser access   | Open a website              | Check browser-based internet access         |
| Snapshot         | VirtualBox interface        | Check the saved recovery point              |

**Note:** These are verification methods. Record a check as successful only after confirming its actual result.

---

## 🐞 Problems Encountered & Solutions

### ⚠️ Problem 1: Understanding NAT Network Configuration

**Challenge:** Initially, I found it confusing to understand the difference between creating a NAT Network in VirtualBox and assigning that network to a virtual machine.

**Action Taken:** I checked the virtual network configuration and the network adapter settings assigned to Kali Linux.

**Learning:** I understood that creating a virtual network and connecting a virtual machine to it are separate configuration steps.

### ⚠️ Problem 2: Different IP Address from the Sample

**Challenge:** The instructor's sample displayed `10.0.0.2`, whereas my Kali Linux environment showed `10.0.2.3`.

**Action Taken:** I used the `ip a` command to inspect the IP address actually assigned to my system.

**Learning:** I learned to verify the actual network configuration instead of assuming that every lab uses identical IP addresses.

### ⚠️ Problem 3: Identifying the Network Connection

**Challenge:** I needed to identify the correct network connection inside Kali Linux before checking its settings.

**Action Taken:** I explored the available network settings and identified `Wired connection 1`.

**Learning:** I learned to check the actual connection name before performing network troubleshooting.

---

## 💡 What I Learned

This project helped me understand virtualization, virtual networking, IP addressing, connectivity verification, and basic troubleshooting.

The most valuable experience was learning to investigate configuration differences instead of copying values directly from sample documentation.

I also learned the importance of verifying actual results, documenting technical steps clearly, and preserving a virtual machine state before further experimentation.

---

## 🔐 Security & Ethical Use

This laboratory is intended for educational purposes and authorized cybersecurity testing only.

All future security assessments will be conducted only on systems that I own or have explicit permission to test.

---

## 🧰 Tools & Resources

* **Oracle VirtualBox:** https://www.virtualbox.org/wiki/Downloads
* **Kali Linux:** https://www.kali.org/get-kali/
* **GitHub:** https://github.com/

---

## 👩‍💻 Author

**Dharshini R P**

Cybersecurity Student

Networkwalks Cybersecurity Program — Batch B082

🔗 **LinkedIn:** https://www.linkedin.com/in/iamdharshini/

---

## 📂 Project Information

* **Project:** Cybersecurity Lab Environment Setup
* **Program:** Networkwalks Cybersecurity Program
* **Batch:** B082
* **Week:** 01
* **Host Operating System:** Windows 11
* **Virtualization Platform:** Oracle VirtualBox
* **Guest Operating System:** Kali Linux







