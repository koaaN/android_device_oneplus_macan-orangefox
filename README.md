# OnePlus 15R/ACE6T macan OrangeFox device tree

## Working

- [X] Display
- [X] Touch 
- [?] Flashing
- [?] Backup & Restore
- [?] KernelSU, KernelSU Next & SukiSU Ultra Installer
- [?] MTP/OTG Storage
- [?] ADB/FastbootD
- [?] Factory Reset
- [?] Vibrator
- [?] Display & Vibration Settings
- [?] Flashlight

## Not working

- [ ] Decryption

# How To Build

### Clone & Sync Source
```
mkdir -p ~/android/OrangeFox_14
cd ~/android/OrangeFox_14
git clone https://gitlab.com/OrangeFox/sync.git
cd sync
./orangefox_sync.sh --branch 14.1 --path ~/android/fox_14.1
```
### Clone Device-tree
```
cd ~/android/fox_14.1/device
mkdir -p oneplus
cd oneplus
git clone https://github.com/koaaN/android_device_oneplus_macan-orangefox macan
```
### BUILD!
```
cd ~/android/fox_14.1
source build/envsetup.sh
lunch twrp_macan-ap2a-eng
mka adbd recoveryimage
```
