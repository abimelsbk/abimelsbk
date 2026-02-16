---
title: "How to Download and Set Up Kali Linux in VirtualBox (Step-by-Step)"
seoTitle: "Download and Set Up Kali Linux in VirtualBox"
seoDescription: "How to Download and Set Up Kali Linux in VirtualBox (Step-by-Step)"
datePublished: Mon Feb 16 2026 08:59:26 GMT+0000 (Coordinated Universal Time)
cuid: cmloy0ogx000f02l60iuabhlt
slug: how-to-download-and-set-up-kali-linux-in-virtualbox
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1771232178779/0d67dda8-6ded-45fb-930a-bd9f0d1720c3.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1771232338867/ce8cd8a7-e3a0-4799-aed4-86da6183734c.png
tags: kali-linux, virtualbox, hacking-lab

---

**How to Download and Set Up Kali Linux in VirtualBox (Step-by-Step)**

Kali Linux is the industry-standard Linux distribution for **penetration testing, ethical hacking, digital forensics, and cybersecurity training**. Running Kali inside **VirtualBox** is the safest and cleanest way to learn, no risk to your main OS, no messy dual-boot issues.

This guide covers:

* What you need before starting
    
* Two installation methods (Easy & Manual)
    
* Common mistakes and fixes
    
* Post-installation best practices
    

## What You Need Before Starting

Make sure this checklist is **100% done** before you start:

### System Requirements (Minimum)

* **64-bit CPU** (Intel or AMD)
    
* **8 GB RAM** (4 GB works, but painfully slow)
    
* **40 GB free disk space**
    
* **Virtualization enabled in BIOS** (for most latest laptops it will be enabled by default)
    

### Software Required

* VirtualBox
    
* Kali Linux (prebuilt image or installer ISO)
    

## How to Check If Virtualization Is Enabled (Before Installing VirtualBox and Kali)

VirtualBox **will not work properly** unless CPU virtualization (Intel VT-x / AMD-V) is enabled. Check this first, don’t skip it.

1. Press **Ctrl + Shift + Esc** → open **Task Manager**
    
2. Go to the **Performance** tab
    
3. Click **CPU**
    
4. Look at the bottom-right
    

You should see:

```plaintext
Virtualization: Enabled
```

If it says **Disabled**, VirtualBox will not show 64-bit options.

## Step 1: Download and Install VirtualBox

![Image](https://miro.medium.com/v2/resize%3Afit%3A1400/1%2AK9IWfgYD3aJdDWkp5UjKZg.png align="left")

![Image](https://cs.hofstra.edu/docs/images/vbox_windows_images/vbox-intro.png align="left")

![Image](https://learn-attachment.microsoft.com/api/attachments/9837eb89-6f80-49ec-ba24-df69b50852c4?platform=QnA align="left")

1. Go to the official VirtualBox website
    
2. Download **VirtualBox for Windows hosts**
    
3. Run the installer
    
4. Keep **all default options** enabled
    
5. Allow network driver installation when prompted
    
6. Restart your system after installation
    

> If VirtualBox doesn’t show **64-bit options later**, your virtualization is disabled in BIOS.

## Step 2: Choose How You Want to Install Kali Linux

You have **two ways**. Pick one based on your goal.

### Option A (Recommended): Pre-Built Kali VirtualBox Image

* Fastest
    
* No manual installation
    
* Perfect for beginners, workshops, labs
    

### Option B: Kali Installer ISO

* Manual Linux installation
    
* Useful if you want to learn Linux internals
    
* More chances to break things
    

**If you’re learning cybersecurity, go with Option A.**

---

## Option A: Install Kali Using Pre-Built VirtualBox Image (Easy Method)

![Image](https://www.kali.org/docs/virtualization/import-premade-virtualbox/import-vbox-weekly-1.png align="left")

![Image](https://unbcybersec.com/blog/training/setting-up-kali/images/download-vms.png align="left")

![Image](https://cdn.diskinternals.com/media/en/products/vmfs-recovery/vmfs-982-min.jpeg align="left")

### Step A1: Download Kali VirtualBox Image

1. Go to Kali Linux official downloads
    
2. Choose **Installer → Virtual Machines**
    
3. Download **Kali Linux VirtualBox Image (64-bit)**
    
    * File size: ~3–4 GB
        
    * Format: `.7z`
        

### Step A2: Extract the File

* Right-click → Extract using **7-Zip or WinRAR**
    
* You’ll get a `.vbox` file and virtual disk files
    

### Step A3: Import into VirtualBox

1. Open VirtualBox
    
2. Click **Machine → Add**
    
3. Select the `.vbox` file
    
4. Kali VM appears in the list
    

### Step A4: Adjust VM Settings (Important)

Before starting Kali:

**System → Motherboard**

* RAM: **4096 MB (minimum)**
    
* Boot Order: Optical → Hard Disk
    

**System → Processor**

* CPUs: **2 or more**
    
* Enable **PAE/NX**
    

**Display**

* Video Memory: **128 MB**
    
* Graphics Controller: **VMSVGA**
    

### Step A5: Start Kali

* Click **Start**
    
* Login credentials:
    
    ```plaintext
    username: kali
    password: kali
    ```
    

✅ Kali is ready to use.

## Option B: Install Kali Using Installer ISO (Manual Method)

![Image](https://www.kali.org/docs/installation/hard-disk-install/boot-installer.png align="left")

![Image](https://docs.oracle.com/en/virtualization/virtualbox/6.0/user/images/create-vm-1.png align="left")

![Image](https://www.kali.org/docs/installation/hard-disk-install/setup-default-metapackages.png align="left")

### Step B1: Download Kali Installer ISO

* Download **Kali Linux Installer (64-bit)**
    
* File size: ~4 GB
    

### Step B2: Create New VM

1. Open VirtualBox → **New**
    
2. Name: `Kali Linux`
    
3. Type: `Linux`
    
4. Version: `Debian (64-bit)`
    

### Step B3: Allocate Resources

* RAM: **4096 MB**
    
* CPU: **2**
    
* Disk: **VDI → Dynamically Allocated → 40 GB**
    

### Step B4: Attach ISO

* Settings → Storage
    
* Under Controller IDE → Empty
    
* Choose Kali ISO file
    

### Step B5: Start Installation

1. Start VM
    
2. Select **Graphical Install**
    
3. Choose:
    
    * Language
        
    * Location
        
    * Keyboard
        
4. Network: Auto (DHCP)
    
5. User setup:
    
    * Username: `kali`
        
    * Password: set strong password
        
6. Partition:
    
    * Guided → Use entire disk → All files in one partition
        
7. Install GRUB → Yes → Select disk
    

### Step B6: Finish Installation

* Remove ISO after installation
    
* Reboot
    
* Login to Kali
    

## Step 3: Install VirtualBox Guest Additions (Mandatory)

Without this, Kali will:

* Lag
    
* Have low resolution
    
* No fullscreen
    
* No clipboard sharing
    

![Image](https://www.virtualbox.org/manual/images/dnd-modes.png align="left")

![Image](https://storage.googleapis.com/ubuntu-18/images/insert-guest-additions-cd-image-ubuntu-18.png align="left")

![Image](https://kbmisc.com/blog/01-install-virtualbox-guest-additions-kali-linux.webp align="left")

### Installation Steps

1. Start Kali
    
2. Menu → **Devices → Insert Guest Additions CD Image**
    
3. Open terminal and run:
    

```bash
sudo apt update
sudo apt install -y build-essential dkms linux-headers-$(uname -r)
sudo mkdir /media/cdrom
sudo mount /dev/cdrom /media/cdrom
sudo sh /media/cdrom/VBoxLinuxAdditions.run
sudo reboot
```

After reboot → Enable **Fullscreen Mode**

## Step 4: Enable Clipboard & Drag-Drop

1. VM Settings → General → Advanced
    
2. Clipboard: **Bidirectional**
    
3. Drag and Drop: **Bidirectional**
    

## Common Problems & Fixes

### 1\. No 64-bit Option in VirtualBox

**Fix**

* Enable **Intel VT-x / AMD-V** in BIOS
    
* Disable **Hyper-V**, **WSL**, **Virtual Machine Platform** in Windows Features
    

### 2\. Kali Black Screen

**Fix**

* Display → Graphics Controller → **VMSVGA**
    
* Disable **3D Acceleration**
    

### 3\. Internet Not Working

**Fix**

* Network Adapter → **NAT**
    
* Restart NetworkManager:
    

```bash
sudo systemctl restart NetworkManager
```

## Best Practices After Installation

* Update Kali:
    

```bash
sudo apt update && sudo apt full-upgrade -y
```

* Take **VirtualBox snapshots** before experiments
    
* Never run attacks outside lab environments
    
* Use platforms like:
    
    * TryHackMe
        
    * Hack The Box
        
    * VulnHub
        

## Final Thoughts

Kali Linux on VirtualBox gives you a clean, controlled, and professional learning environment that mirrors how real-world security teams work, without putting your main system at risk. Once set up properly, this single virtual machine becomes your all-in-one lab for learning Linux, practicing ethical hacking, testing tools, and building real cybersecurity skills step by step. Mastering Kali in a VM also teaches you an important industry habit early, work in isolated environments, take snapshots before experiments, break things safely, and recover fast. If you’re serious about cybersecurity, this setup isn’t optional; it’s the foundation you’ll keep using as you move from beginner labs to advanced, real-world scenarios.