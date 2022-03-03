# Dell-7080-Series-EFI

Boot loader: OpenCore

# Kexts-and-plist
i7-10700 + Dell 7080 Tower

Components used for this build:

- CPU: Intel(R) Core(TM) i7-10700 CPU @ 2.9GHz
- Motherboard: Dell 7080
- Memory: 32 GB DDR4 2666MHZ
- Storage: Samsung 98 1T NVME + 1TB HDD
- GPU: UHD 630
- WIFI: BCM943602CS 双频10DB

# BIOS 设置

- System Configuration → SATA Operation: AHCI
- Secure Boot → Secure Boot Enable: Disabled
- System Configuration → SerialPort Disabled （建议)
- Secure → PTT Secure(TPM) Disabled （建议)
- Secure → Intel SGX Disabled （建议)
- System Configuration → PCI Slot Disabled (如果PCI插槽为空，仅TM系列)

# 修改 DVMT 和解锁 CFG LOCK
  将 Ru.efi 在BIOS中添加进Boot Menus 后启动 进入Ru后按 "Alt" + "=" 并查找 CPUSetup 和 SaSetup

- 解锁"CFG-LOCK" 找到CPUSetup 将横排 "0030" "0E" 位改为 00
- 修改DVMT 搜索 SaSetup 将横排 "00F0" "05" 位改为 "02"

## 3 Mar 2022 Update:
- OpenCore 0.7.8
- Kexts update
- Drivers update
- macOS 12.2.1