# how-to-flash-custom-roms
A guide to show y'all how to flash custom roms and root it on a21s, wish it helps.
# Flashing Custom ROM: Step by Step Guide

> Ensure you have a **PC**, **USB cable**, **Some brain cells**, and **backed-up data** (process wipes all data).

---

## Table of Contents
- [Preparations](#preparations)
  - [Unlock Bootloader](#1-unlock-bootloader)
  - [Enable Developer Options & USB Debugging](#2-enable-developer-options--usb-debugging)
- [Flashing Custom Recovery](#flashing-custom-recovery)
  - [Prepare Recovery](#1-prepare-recovery)
  - [Flash via Odin (Windows)](#2-flash-via-odin-windows)
  - [Boot into Recovery](#3-boot-into-recovery)
- [Flashing the ROM and gapps](#flashing-the-rom-and-gapps)
  - [In Recovery](#1-in-recovery)
  - [Sideload ROM via ADB](#2-sideload-rom-via-adb)
  - [Installing GApps (If Required)](#3-installing-gapps-if-required)
- [Rooting with Magisk (Optional)](#rooting-with-magisk-optional)
  - [Prepare Magisk](#1-prepare-magisk)
  - [Flash Magisk in Recovery](#2-flash-magisk-in-recovery)
  - [Finalize](#3-finalize)

---

## Preparations

### 1. Unlock Bootloader
- Power off device.  
- Hold **Volume Up + Volume Down** while plugging into PC.  
- Use volume keys to select **"Unlock Bootloader"** → Confirm.  

**WARNING: This erases all data!**

---

### 2. Enable Developer Options & USB Debugging
- Go to **Settings → About Phone → Build Number**.  
- Tap **"Build Number"** 7 times to enable Developer Options.  
- In Developer Options, enable **USB Debugging**.  

---

## Flashing Custom Recovery  
**Tools needed:** Odin (Windows) 

### 1. Prepare Recovery
- Compress `recovery.img` (link in downloads section) to `recovery.tar`  
  → Right click on `recovery.img` then choose **compress to .tar**.  

### 2. Flash via Odin (Windows)
- Open Odin → Disable **"Auto Reboot"** in Options.  
- Load `recovery.tar` into the **AP slot**.  
- Click **Start**.  

### 3. Boot into Recovery
- After flashing, hold **Power + Volume Down** until screen turns black.  
- Immediately switch to **Power + Volume Up** to enter Recovery.  

---

## Flashing the ROM and gapps  
**Tools needed:** Platform-Tools (ADB)

### 1. In Recovery
- Wipe Data → Format Data → Yes.  
- Apply Update → Apply from ADB.  

### 2. Sideload ROM via ADB
- Extract the `.zip` file then right click to an empty space in folder then choose **open terminal**.  
- Type `cmd` then enter.  
- After that type `adb sideload` then go to the place where you downloaded the rom and grab it with the mouse.  
- When you put it in the terminal tab you will notice that its name is now located after the `adb sideload` command.  
- Press enter and the rom will start flashing.  

### 3. Installing GApps (If Required)  
*Skip if i wrote in ROM notes that it includes GApps.*  

1. Sideload GApps Immediately:  
   - After ROM flash, stay in Recovery → Apply Update → Apply from ADB.  
   - I will leave gapps download link in download section, and with the same steps that you flashed the rom in the terminal you opened type `adb sideload` grab the file with the mouse then enter.  
   - When its done youre ready to press **reboot the system**.  

---

## Rooting with Magisk (Optional)

### 1. Prepare Magisk
- Download Magisk v26.3  
- Rename `Magisk-v26.3.apk` → `Magisk-v26.3.zip` (using ZArchiver).  
- Copy ZIP to device/SD card.  

### 2. Flash Magisk in Recovery
- Reboot to Recovery:  
  - **Power + Volume Up** or use ROM’s *Advanced Reboot* feature.  
- Navigate:  
  - Apply Update → Choose from Internal/SDCard → Select **Magisk ZIP**.  

### 3. Finalize
- Reboot system → Open Magisk app → Complete setup.  

---

> Enjoy your custom ROM :3

