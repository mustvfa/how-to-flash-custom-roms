# Flashing Custom ROM: Step by Step Guide

> A guide to show y'all how to flash custom ROMs and root it on Galaxy A21s.  
> Tested on **Samsung Galaxy A21s (SM-A217F/DS)**.  

---

> ## ⚠ Warnings & Disclaimer
- Unlocking the bootloader will **void warranty**.  
- This process will **erase all data** on your phone.  
- Flashing custom software can **brick your device** if done wrong.  
- Proceed at your own risk — I am **not responsible** for any damages.  

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
- Hold **Volume Up + Volume Down** while plugging into PC — now you’re in Download Mode.  
- Hold **Volume Up key**, then press it again — device will restart with bootloader unlocked.  

---

## Flashing Custom Recovery  
**Tools needed:** [Odin (Windows)](https://odindownload.com/download/Odin3_v3.14.4.zip)  

### 1. Prepare Recovery
- Compress `recovery.img` (from Downloads section in Telegram/XDA) to `recovery.tar`.  
  → Right click `recovery.img` → **Compress to .tar**.  

### 2. Flash via Odin (Windows)
- Open Odin → go to **Options** → **Disable Auto Reboot**.  
- Put `recovery.tar` into the **AP slot**.  
- Click **Start**.  

### 3. Boot into Recovery
- When Odin shows **PASS**, hold **Power + Volume Down** until screen turns black.  
- Immediately switch to **Power + Volume Up** until Recovery loads.  

---

## Flashing the ROM and GApps  
**Tools needed:** [Platform-Tools (ADB)](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)  

### 1. In Recovery
- Wipe Data → Format Data → Yes.  
- Apply Update → Apply from ADB.  

### 2. Sideload ROM via ADB
- Extract **platform-tools-latest-windows.zip**.  
- Right click inside the folder → **Open Terminal**.  
- Type `cmd` then press Enter.  
- Type `adb sideload` then drag your ROM `.zip` file into the terminal window.  
- Press Enter → ROM starts flashing.  

### 3. Installing GApps (If Required)  
- Skip if ROM notes say it already includes GApps.  
- After ROM flash → stay in Recovery → Apply Update → Apply from ADB.  
- Sideload GApps `.zip` the same way as ROM.  
- When done, select **Reboot system now**.  

---

## Rooting with KSU (Optional)
- Right after flashing ROM (and GApps if needed), sideload [Atlas](https://github.com/samsungexynos850/atlas/releases/tag/stable).  
- Wipe Data → Format Data.  
- Boot system → install KSU app from [Atlas release](https://github.com/samsungexynos850/atlas/releases/tag/stable).  
- You now have root access with KernelSU.  

---

## Rooting with Magisk (Optional)

### 1. Prepare Magisk
- Download **Magisk v26.3**.  
- Rename `Magisk-v26.3.apk` → `Magisk-v26.3.zip`.  
- Copy ZIP to device/SD card.  

### 2. Flash Magisk in Recovery
- Boot into Recovery (**Power + Volume Up**) or use ROM’s Advanced Reboot.  
- Go to **Apply Update → Choose from Internal/SDCard** → Select Magisk ZIP.  

### 3. Finalize
- Reboot system.  
- Open Magisk app → complete setup.  

---

> Enjoy your custom ROM!  

---

## Table of Contents
- [Preparations](#preparations)  
  - [Enable Developer Options](#1-enable-developer-options)  
  - [Unlock Bootloader](#2-unlock-bootloader)  
- [Flashing Custom Recovery](#flashing-custom-recovery)  
  - [Prepare Recovery](#1-prepare-recovery)  
  - [Flash via Odin (Windows)](#2-flash-via-odin-windows)  
  - [Boot into Recovery](#3-boot-into-recovery)  
- [Flashing the ROM and GApps](#flashing-the-rom-and-gapps)  
  - [In Recovery](#1-in-recovery)  
  - [Sideload ROM via ADB](#2-sideload-rom-via-adb)  
  - [Installing GApps (If Required)](#3-installing-gapps-if-required)  
- [Rooting with KSU (Optional)](#rooting-with-ksu-optional)  
- [Rooting with Magisk (Optional)](#rooting-with-magisk-optional)  
  - [Prepare Magisk](#1-prepare-magisk)  
  - [Flash Magisk in Recovery](#2-flash-magisk-in-recovery)  
  - [Finalize](#3-finalize)  
