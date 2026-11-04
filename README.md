# Networkwalks-B0841-week1-Cybersecurity-lab-set-up
# Kali Linux Lab Setup

**Student:** Aubrey Membe
**Course:** Cybersecurity lab setup / BO841
**Date:** 4 November 2026

## 1. Objective
Set up a Kali Linux virtual machine in VirtualBox for security lab practice.

## 2. Environment
| Item | Details |
|------|---------|
| Host OS | Windows 11 |
| Hypervisor | Oracle VirtualBox 7.2 |
| Guest OS | Kali Linux 2026.2 (amd64) |
| RAM / CPU | 4 GB / 2 cores |
| Disk | 50 GB dynamic |
| Network | NAT |

## 3. Steps Performed
1. Downloaded the Kali VirtualBox image from kali.org
2. Imported the VM into VirtualBox
3. Configured RAM, CPU and network adapter
4. Booted the VM and updated the system:
   ```
   sudo apt update && sudo apt full-upgrade -y
   ```
5. Installed Guest Additions:
   ```
   sudo apt install -y --reinstall virtualbox-guest-x11 virtualbox-guest-utils
   sudo reboot
   ```
6. Set up a shared folder (`sf_shared`)
7. Created this Git repo to document the work

## 4. Problems and Fixes
| Problem | Cause | Fix |
|---------|-------|-----|
| `Unable to locate package virtualbox-guest` | Wrong package name and misplaced `reinstall` | Used `virtualbox-guest-x11` with `--reinstall` |

## 5. Screenshots


![Kali desktop](screenshots/desktop.png)




![Guest Additions installed](screenshots/guest-additions.png)



## 6. Files in This Repo
- `notes/` : command history, system info, package list
- `configs/` : configuration files I edited
- `screenshots/` : evidence of each step

## 7. What I Learned
Short paragraph in your own words.
