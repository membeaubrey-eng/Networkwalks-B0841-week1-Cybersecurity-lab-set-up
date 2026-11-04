<h1 align="center">🛡️ Kali Linux Security Lab</h1>

<p align="center">
  <i>A hands-on virtual lab for learning networking and ethical hacking</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HYPERVISOR-VirtualBox-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/OS-Kali%20Linux-557C94?style=for-the-badge">
  <img src="https://img.shields.io/badge/STATUS-In%20Progress-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/LEVEL-Beginner-green?style=for-the-badge">
</p>

---

## 📌 Overview
This repository documents how I built an isolated cybersecurity lab using **Kali Linux** and **Oracle VirtualBox**. It records each step, the problems I met, and how I fixed them.

> ⚠️ **Disclaimer:** This lab is for education and authorized testing only.

---

## 🎯 Objectives
- ✅ Install and configure VirtualBox
- ✅ Deploy a Kali Linux virtual machine
- ✅ Install Guest Additions (clipboard, shared folders, resizing)
- ✅ Document the work with Git and GitHub
- ⬜ Add a vulnerable target VM
- ⬜ Practice scanning with Nmap

---

## 🧰 Requirements
| Component | Details |
|-----------|---------|
| 💻 Host OS | Windows 11 |
| 📦 Hypervisor | VirtualBox 7.2 |
| 🐉 Guest OS | Kali Linux 2026.2 (amd64) |
| 🧠 RAM | 4 GB |
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
| Adapter 2 | Host-Only | Isolated lab network |

---

## 🛠️ Tools Used
`Nmap` · `Wireshark` · `Metasploit` · `Burp Suite` · `Git`

---

## 🧩 Troubleshooting
| ❌ Problem | 🔍 Cause | ✅ Fix |
|-----------|----------|--------|
| `Unable to locate package virtualbox-guest` | Wrong package name | Used `virtualbox-guest-x11` |
| No internet in VM | Adapter not set to NAT | Changed adapter to NAT |

---

## 📸 Screenshots
| Kali Desktop | Guest Additions |
|:---:|:---:|
| 

![desktop](screenshots/desktop.png)

 | 

![ga](screenshots/guest-additions.png)

 |

---

## 🗺️ Roadmap
- [x] Week 1: Lab setup
- [ ] Week 2: Add a vulnerable VM
- [ ] Week 3: Network scanning
- [ ] Week 4: Vulnerability assessment

---

## 📚 What I Learned
Write 3 to 4 sentences in your own words about what you learned and what challenged you.
i learnt how tp setup the lab using vitual box and kali linux. i had challenges on upgrading the kali nux but eventualy i managed as command prompt could not locate guest file
---

## 👤 Author
**Aubrey Membe **
Course: NETWORKWALKS CYBERSECURITY B0841 WEEK 1 LAB SETUP
GitHub: [mebeaubrey-eng](https://github.com/membeaubrey-eng)
