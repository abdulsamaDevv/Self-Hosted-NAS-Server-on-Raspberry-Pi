# Raspberry Pi NAS with OpenMediaVault

A fully open-source NAS powered by OpenMediaVault on Ubuntu Server + Raspberry Pi. Web UI makes storage, sharing, and backups easy!

## 🧰 Requirements

- Raspberry Pi 4 or 5
- microSD card (16 GB or larger)
- External USB SSD/HDD (powered)
- Ubuntu Server 22.04 LTS (ARM64)
- Ethernet or Wi-Fi connection
- Computer for flashing OS

---

## 🚀 Setup Instructions

### ✅ Step 1: Flash Ubuntu Server to SD Card

Use [Raspberry Pi Imager](https://www.raspberrypi.com/software/) to flash Ubuntu Server:

1. Choose OS → Ubuntu Server 22.04 (64-bit)
2. Choose storage → your microSD card
3. (Optional) Configure hostname, SSH, and Wi-Fi

`docs/screenshots/Pi Imager`_

---

### ✅ Step 2: Boot the Pi and Update

Insert the SD card into your Pi and power it on.

Update the system by running the following commands in the terminal:

```bash
sudo apt update && sudo apt upgrade -y

