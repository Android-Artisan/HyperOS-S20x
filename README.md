
<h1 align="center">HyperOS Port for Galaxy S20 Series (Exynos/Snapdragon Soon)</h1>
<h3 align="center">Early Tester Build | Fastboot Flashable system.img | TWRP/PBRP Flashable Kernel boot.img/dtbo.img</h3>

---

## 📱 Supported Devices

**Tested (Exynos Variants):**
- Samsung Galaxy S20 4G/5G - x1s/lte - SM-G980F/SM-G981B
- Samsung Galaxy S20+ 4G/5G - y2s/lte - SM-G985F/SM-G986B
- Samsung Galaxy S20U - z3s - SM-G988B

**Untested (Exynos Variants):**
- Samsung Galaxy Note 20 4G/5G - SM-N980F/SM-N981B
- Samsung Galaxy Note 20U 4G/5G - SM-N985F/SM-N986B
---

## 🏗 Current Status

**Working:**
- UI boots normally  
- Front camera  
- Touchscreen + navigation
- ArtisanKernel V0.0.2

**Broken / WIP:**
- Play integrity
- Play Protect certification
- IMEI Broken
- Xiaomi Account
- Google Account
- Rear cameras  
- Fingerprint sensor  
- Flashlight  
- SIM/network (SIM fix non-functional)  
- VoLTE / VoWiFi  
- Some sensors  

---

##  Flashing Instructions

> **Note:** This is a raw `system.img`. It must be flashed via **Fastboot**. Make sure to back up your data and know what you're doing.

## [HyperOS Download](https://drive.usercontent.google.com/download?id=1evFw-23jmfMp_prehsbECpYtNo04d7L6&export=download&authuser=9)
## [ArtisanKernel Download](https://github.com/Android-Artisan/android_kernel_samsung_exynos990/releases)

### Requirements:
- Unlocked bootloader  
- ADB & Fastboot installed on your PC  
- Compatible vendor and boot image already in place  (Flash Ronnz Lineage OS 21 first)

### Steps:
- Download the GSI above
- Download Lineage OS 21 Ronnz
- Flash Lineage OS
- Flash ArtisanKernel
- Flash system.img

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
- Flash multidissabler
- Flash permissiver
- and then boot

---

## 📋 Notes

- Kernel Built
- Not a daily driver , for development/testing only  
- Feedback and logs are welcome and helpful  

---

## 👥 Credits

- Ported by: Android Artisan
- GSI System image originally from MysticGSI
- Kernel By: ExtremeXT
  
### Contributors
- NeverLose
- YacineGTI
- The Exynos Hater

### Thank You To
- HyperOS by Xiaomi  
- Tools from Samsung & open-source community
- MysticGSI

---

## ⚠️ Disclaimer

> This is a **tester build** in early development. Flash at your own risk. We are **not responsible** for bricked devices, bootloops, or any damage.
