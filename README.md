
<h1 align="center">HyperOS Port for Galaxy S20 Series (Exynos)</h1>
<h3 align="center">Early Tester Build | Fastboot Flashable system.img</h3>

---

## 📱 Supported Devices

**Tested (Exynos Variants):**
- Samsung Galaxy S20 4G - x1slte - SM-G980F
- Samsung Galaxy S20 5G - x1s - SM-G981B
- Samsung Galaxy S20+ 5G - y2s - SM-G986B
- Samsung Galaxy S20U - z3s - SM-G988B

**Untested (Exynos Variants):**
- Samsung Galaxy S20+ 4G - y2slte - SM-G985F
---

## 🏗 Current Status

**Working:**
- UI boots normally  
- Front camera  
- Touchscreen + navigation  

**Broken / WIP:**
- IMEI Broken
- Xiaomi Account
- Google Account
- Rear cameras  
- Fingerprint sensor  
- Flashlight  
- SIM/network (SIM fix non-functional)  
- VoLTE / VoWiFi  
- Some sensors  
- No bundled kernel (use external)  

---

##  Flashing Instructions

> **Note:** This is a raw `system.img`. It must be flashed via **Fastboot**. Make sure to back up your data and know what you're doing.

## [HyperOS Download](https://drive.usercontent.google.com/download?id=1evFw-23jmfMp_prehsbECpYtNo04d7L6&export=download&authuser=9)

### Requirements:
- Unlocked bootloader  
- ADB & Fastboot installed on your PC  
- Compatible vendor and boot image already in place  (Flash Ronnz Lineage OS 21 first)

### Steps:
- Download the gsi above
- Download lineage os 21 Ronnz
- flash lineage os
- flash system img

```bash
# Reboot to Recovery
./adb reboot bootloader

# Once in Recovery reboot to FastBootD

# Erase partitions
./fastboot erase system
./fastboot delete-logical-partition product
./fastboot delete-logical-partition system_ext

# Flash system image
./fastboot flash system /Path/To/system.img

# Reboot to recovery
./fastboot reboot recovery

# Erase and factory reset in wipe then type "yes"
```
- flash multidissabler
- flash permissiver
- and then boot

---

## 📋 Notes

- No kernel included , use a compatible one  
- Not a daily driver , for development/testing only  
- Feedback and logs are welcome and helpful  

---

## 👥 Credits

- Ported by: Android Artisan
- GSI System image originally from MysticGSI
  
### Contributors
- NeverLose
- YacineGTI
- TheExynosHater

### Thank You To
- HyperOS by Xiaomi  
- Tools from Samsung & open-source community
- MysticGSI

---

## ⚠️ Disclaimer

> This is a **tester build** in early development. Flash at your own risk. We are **not responsible** for bricked devices, bootloops, or any damage.
