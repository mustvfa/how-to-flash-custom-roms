A guide to show y'all how to flash custom roms and root it on a21s, wish it helps.
# Flashing Custom ROM: Step by Step Guide

> Ensure you have a **PC**, **USB cable**, **Some brain cells**, and **backed-up data** (process wipes all data).

---

## Preparations

### 1. Enable Developer Options
- Go to **Settings → About Phone → Software Information → Build Number**.  
- Tap **"Build Number"** 7 times to enable Developer Options.  
- In Developer Options, enable **OEM unlocking and USB Debugging**.  

---

### 2. Unlock Bootloader
> **WARNING: This erases all data!**

- Power off device.  
- Hold **Volume Up + Volume Down** while plugging into PC and now you're in download mode.  
- Hold **Volume up key** and then press **Volume up key**, it will now restart and you'll have unlocked you're bootloader.  

---

## Flashing Custom Recovery  
**Tools needed:** [Odin (Windows)](https://odindownload.com/download/Odin3_v3.14.4.zip) 

### 1. Prepare Recovery
- Compress `recovery.img` (link in downloads section in my telegram or xda post) to `recovery.tar`  
  → Right click on `recovery.img` then choose **compress to .tar**.  

### 2. Flash via Odin (Windows)
- Open Odin → **options** → **Disable Auto Reboot**.  
- Put `recovery.tar` into the **AP slot**.  
- Click **Start**.  

### 3. Boot into Recovery
- After flashing is done and it said pass, hold **Power + Volume Down** until screen turns black.  
- Immediately switch to **Power + Volume Up** till it enters Recovery.  

---

## Flashing the ROM and gapps  
**Tools needed:** [Platform-Tools (ADB)](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)

### 1. In Recovery
- Wipe Data → Format Data → Yes.  
- Apply Update → Apply from ADB.  

### 2. Sideload ROM via ADB
- Extract **platform-tools-latest-windows.zip** file then right click to an empty space in folder then choose **open terminal**.  
- Type `cmd` then enter.  
- After that type `adb sideload` then go to the place where you downloaded the rom and grab it with the mouse and put it in terminal tab.  
- When you put it in the terminal tab you will notice that its name is now located after the `adb sideload` command.  
- Press enter and the rom will start flashing.  

### 3. Installing GApps (If Required)  
> *Skip if i wrote in ROM notes that it includes GApps.*  

1. Sideload GApps Immediately:  
   - After ROM flash, stay in Recovery → Apply Update → Apply from ADB.  
   - I will leave gapps download link in download (in telegram or xda post) section, and with the same steps that you flashed the rom in the terminal you opened type `adb sideload` grab the file with the mouse then enter.  
   - When its done youre ready to press **reboot the system**.  

---

## Rooting with Ksu (Optional)
-Straight after you've flashed the rom and gapps, Flash [atlas](https://github.com/samsungexynos850/atlas/releases/tag/stable), then wipe data → format data.
-Then boot system download ksu app which is [here](https://github.com/samsungexynos850/atlas/releases/tag/stable) and you have root access. 

## Rooting with Magisk (Optional)

### 1. Prepare Magisk
- Download Magisk v26.3  
- Rename `Magisk-v26.3.apk` → `Magisk-v26.3.zip` (using ZArchiver).  
- Copy ZIP to device/SD card.  

### 2. Flash Magisk in Recovery
- Reboot to Recovery:  
  - power off the hold **Power + Volume Up** or use ROM’s *Advanced Reboot* feature.  
- Navigate:  
  - Apply Update → Choose from Internal/SDCard → Select **Magisk ZIP**.  

### 3. Open magisik app
- Reboot system → Open Magisk app → Complete setup.  

---

> Enjoy your custom ROM :3

---

## Table of Contents
- [Preparations](#preparations)
  - [Enable Developer Options](#1-enable-developer-options)
  - [Unlock Bootloader](#2-unlock-bootloader)
- [Flashing Custom Recovery](#flashing-custom-recovery)
  - [Prepare Recovery](#1-prepare-recovery)
  - [Flash via Odin (Windows)](#2-flash-via-odin-windows)
  - [Boot into Recovery](#3-boot-into-recovery)
- [Flashing the ROM and gapps](#flashing-the-rom-and-gapps)
  - [In Recovery](#1-in-recovery)
  - [Sideload ROM via ADB](#2-sideload-rom-via-adb)
  - [Installing GApps (If Required)](#3-installing-gapps-if-required)
- [Rooting with Ksu (Optional)](#rooting-with-ksu-optional)
- [Rooting with Magisk (Optional)](#rooting-with-magisk-optional)
  - [Prepare Magisk](#1-prepare-magisk)
  - [Flash Magisk in Recovery](#2-flash-magisk-in-recovery)
  - [Open Magisk app](#3-open-magisk-app)
