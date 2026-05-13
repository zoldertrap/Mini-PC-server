# Mini-PC-server
# Mini-PC-server
# Mini-PC Proxmox Server

A small homelab / server setup using Proxmox VE on a mini PC.

---

# Hardware

- Mini PC
- SSD storage
- Ethernet connection
- USB flash drive (8GB+)

---

# Download Proxmox

Download the latest Proxmox VE ISO:

https://www.proxmox.com/en/downloads

---

# Create Bootable USB

## Windows

Use Rufus:

https://rufus.ie

1. Insert USB drive
2. Select Proxmox ISO
3. Start flashing

---

# BIOS Configuration

Before installing:

- Enable virtualization:
  - Intel VT-x / VT-d
  - AMD-V / IOMMU
- Set USB as first boot device
- Disable Secure Boot if needed

---

# Install Proxmox

1. Boot from USB
2. Select:

```text
Install Proxmox VE
```

3. Accept license agreement
4. Select target disk
5. Configure:
   - Country
   - Timezone
   - Keyboard layout
6. Set:
   - Root password
   - Email address
7. Configure network:
   - Hostname
   - Static IP recommended

Example:

```text
Hostname: proxmox.local
IP: 192.168.1.100
```

8. Finish installation
9. Reboot system

---

# Access Web Interface

Open browser:

```text
https://YOUR-IP:8006
```

Example:

```text
https://192.168.1.100:8006
```

Login with:

```text
User: root
Password: your-password
```

---

# First Update

Run updates after installation:

```bash
apt update && apt upgrade -y
```

---

# Create First VM

1. Upload ISO images
2. Click "Create VM"
3. Configure:
   - CPU
   - RAM
   - Storage
   - Network
4. Install operating system

---

# Useful Commands

## Check IP

```bash
ip a
```

## Update system

```bash
apt update && apt upgrade -y
```

## Reboot server

```bash
reboot
```

---

# Future Plans

- [ ] Docker VM
- [ ] Home Assistant
- [ ] NAS storage
- [ ] Plex server
- [ ] Backup automation

---

# Notes

This repository documents my personal Proxmox homelab setup and configurations.