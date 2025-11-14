📌 Overview

This repository contains short notes on installing VMware Workstation, creating an Ubuntu virtual machine, and connecting to it using SSH key authentication with MobaXterm.

🛠 Setup Steps
1. Install VMware Workstation

Install VMware Workstation on Windows

Enable Virtualization in BIOS (if required)

2. Create Ubuntu VM

Download the Ubuntu ISO

Create a new virtual machine in VMware

Complete the Ubuntu installation

3. Enable SSH on Ubuntu
sudo apt update
sudo apt install openssh-server -y

4. Connect Using SSH (MobaXterm)

Generate an SSH key using MobaKeyGen

Add your public key to:

~/.ssh/authorized_keys


Connect to your VM:

ssh -i keyfile username@VM-IP

⚠️ Common Issues & Fixes
• Permission denied (publickey)

Fix SSH permissions and restart SSH.

• No IP address

Switch VMware network to NAT or Bridged → check IP with ip a.

• SSH login slow

Disable DNS lookup in sshd_config.

• Keyboard/mouse issues

Install VMware tools:

sudo apt install open-vm-tools-desktop -y

✅ Summary

VMware installed ✔
Ubuntu VM created ✔
SSH enabled ✔
Key-based login working ✔
Common VM/SSH issues resolved ✔
