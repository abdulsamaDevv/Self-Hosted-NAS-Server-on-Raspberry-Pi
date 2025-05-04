Raspberry Pi NAS with OpenMediaVault
A fully open-source NAS powered by OpenMediaVault on Ubuntu Server + Raspberry Pi. Web UI makes storage, sharing, and backups easy!
🧰 Requirements

Raspberry Pi 4 or 5
microSD card (16 GB or larger)
External USB SSD/HDD (powered)
Ubuntu Server 22.04 LTS (ARM64)
Ethernet or Wi-Fi connection
Computer for flashing OS

🚀 Setup Instructions
✅ Step 1: Flash Ubuntu Server to SD Card
Use Raspberry Pi Imager to flash Ubuntu Server:

Choose OS → Ubuntu Server 22.04 (64-bit)
Choose Storage → your microSD card
(Optional) Configure hostname, enable SSH, and connect to Wi-Fi

✅ Step 2: Boot the Pi and Update
Insert the SD card into your Raspberry Pi and power it on.
Update the system packages:
bashsudo apt update && sudo apt upgrade -y
✅ Step 3: Install OpenMediaVault (OMV)
Install required dependencies:
bashsudo apt install curl gnupg -y
Download and run the OMV installation script:
bashcurl -fsSL https://github.com/OpenMediaVault-Plugin-Developers/installScript/raw/master/install | sudo bash
⏳ The installation may take 15–30 minutes. Your Pi will reboot automatically once it's done.
✅ Step 4: Access OMV Web Interface
Open a browser and go to:
http://<your_pi_ip>/
Default login credentials:

Username: admin
Password: openmediavault

✅ Step 5: Configure Storage
Plug in your external USB drive.
In the OMV Web UI:

Go to Storage > Disks to verify the drive is detected.
Navigate to Storage > File Systems:

Create a new file system (ext4 recommended).
Mount the file system.


Go to Access Rights Management > Shared Folders to create shared directories.

✅ Step 6: Enable File Sharing Services
For SMB/CIFS (Windows/macOS/Linux):

Go to Services > SMB/CIFS
Enable the service
Enable "Home directories" if desired
Under Shares, click "Add":

Choose your shared folder
Set guest access or specific permissions



✅ Step 7: Optional – Add Users

Go to Access Rights Management > User
Click Add to create users with access to specific shared folders

🔐 Tips for Better Security

Change the default admin password after first login
Use a static IP or configure your router to reserve one
Regularly back up your OMV config and important data
Use SSH keys for remote access and disable password-based SSH logins
