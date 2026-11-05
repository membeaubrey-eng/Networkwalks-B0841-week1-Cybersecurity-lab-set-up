<h1 align="center">🛡️ Kali Linux Security Lab</h1>

<p align="center">
  <i>A hands-on virtual lab for learning networking and ethical hacking</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HYPERVISOR-VirtualBox-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/OS-Kali%20Linux-557C94?style=for-the-badge">
  <img src="https://img.shields.io/badge/FORCUS-%20CYBERSECURITY-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/ENVIRONMENT-LAB-green?style=for-the-badge">
</p>

---

## 📌 Overview
This repository documents how I built an isolated cybersecurity lab using **Kali Linux** and **Oracle VirtualBox**. It records each step, the problems I met, and how I fixed them. The purpose of the lab is to create a controlled environment where cybersecurity tools network scanning,reconnaisance,vulnerability,assessment and other security testing activities can be performed safely and repeatedly
The Lab is configured on private virtual network so that additional machines can be added and used as targets for authorised testing

> ⚠️ **Disclaimer:** This lab is for education and authorized testing only.

---

## 🎯 Objectives
- ✅ Install and configure VirtualBox
- ✅ Deploy a Kali Linux virtual machine
- ✅ Install Guest Additions (clipboard, shared folders, resizing)
- ✅ Assign a consistent IP address to kali vm
- ✅ Verify network connectivity and DNS resolution
- ✅ Take a clean vm snapshort for recovery
- ✅ Document the complete setup process
- ✅ Prepare the environment for future cybersecurity projects

## 🎯 Purpose of the lab
The lab provides an isolated and controlled environment for cybersecurity learning and authorised testing.
It can be used for activities such as
- ✅ Network Reconnaissence
- ✅ Port scanning
- ✅ Vulnerability assessment
- ✅ Packet analysis
- ✅ Web security testing
- ✅ Exploitation practice
- ✅ Security tool experimentation


## 🧰 Requirements
| Component | Details |
|-----------|---------|
| 💻 Host OS | Windows 11 |
| 📦 Hypervisor | VirtualBox 7.2 |
| 🐉 Guest OS | Kali Linux 2026.2 (amd64) |
| 🧠 Host RAM | 8 GB |
| 🧠 Kali RAM | 2048 MB |
| ⚙️ CPU | 2 cores |
| 💾 Disk | 50 GB |

---

## 🏗️ Lab Architecture
```
┌──────────────────────────────┐
│        Host (Windows)        │
│  ┌────────────────────────┐  │
│  │      VirtualBox        │  │
│  │   ┌────────────────┐   │  │
│  │   │  Kali Linux VM │   │  │
│  │   └────────────────┘   │  │
│  └────────────────────────┘  │
└──────────────────────────────┘
```

---

## ⚙️ Installation Steps

### Step 1: Import the VM
Downloaded the Kali VirtualBox image from kali.org and imported it.

### Step 2: Update the system
```bash
sudo apt update && sudo apt full-upgrade -y
```

### Step 3: Install Guest Additions
```bash
sudo apt install -y --reinstall virtualbox-guest-x11 virtualbox-guest-utils
sudo reboot
```

### Step 4: Configure a shared folder
Machine → Settings → Shared Folders → add `sf_shared`.

---

## 🌐 Network Configuration
| Adapter | Mode | Purpose |
|---------|------|---------|
| Adapter 1 | NAT | Internet access |
| Network Address | 10.0.0.0/24|  |
| Kali IP address | 10.0.0.2/24|  |
| Default gateway | 10.0.0.1 |  |
| DNS Server |8.8.8.8 |  |
| Future VM Range | 10.0.0.3 to 10.0.0.99 |  |



---

## 🛠️ Tools Used
`virtual box` · `kali linux` 

---

## 🧩 Troubleshooting
| ❌ Problem | 🔍 Cause | ✅ Fix |
|-----------|----------|--------|
| `Unable to locate package virtualbox-guest` | Wrong package name | Used `virtualbox-guest-x11` |
| No internet in VM | Adapter not set to NAT | Changed adapter to NAT |

---

## 📸 Screenshots

### 1. Kali Desktop


![Kali desktop](https://github.com/membeaubrey-eng/Networkwalks-B0841-week1-Cybersecurity-lab-set-up/edit/main/README.md#:~:text=Screenshot%202026%2D11%2D04%20202956.png)



### 2. Guest Additions Installed


![Guest Additions](screenshots/guest-additions.png)



### 3. Network Settings


![Network settings](screenshots/network.png)



### 4. Shared Folder


![Shared folder](screenshots/shared-folder.png)



### 5. System Update


![System update](screenshots/update.png)



### 6. Terminal Output


![Terminal output](screenshots/terminal.png)



### 7. Git Push


![Git push](screenshots/git-push.png)

## 🗺️ Roadmap
- [x] Week 1: Lab setup


---

## 📚 What I Learned
i learnt how to setup the lab using vitual box and kali linux. i had challenges on upgrading the kali linux but eventualy i managed as command prompt could not locate guest file virtualbox-guest-x11
---

## 👤 Author
**Aubrey Membe **
Course: NETWORKWALKS CYBERSECURITY B0841 WEEK 1 LAB SETUP
GitHub: [mebeaubrey-eng](https://github.com/membeaubrey-eng)
