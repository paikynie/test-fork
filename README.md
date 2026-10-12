# Nebula Touch 1.2.6 — VIP Mod

Hasil mod APK Nebula Touch v1.2.6 (`com.nebula.hnx`) dengan fitur VIP/Elite terbuka.

## File
| File | Keterangan |
|---|---|
| `NebulaTouch-1.2.6-VIP-MOD.apks` | Bundle lengkap (base + 5 split), install via **SAI** |
| `apk/base.apk` | Base APK (patched + signed) |
| `apk/split_config.arm64_v8a.apk` | Native libs (arm64) |
| `apk/split_config.en.apk` | Locale English |
| `apk/split_config.in.apk` | Locale Indonesia |
| `apk/split_config.ms.apk` | Locale Malay |
| `apk/split_config.xhdpi.apk` | Resource density xhdpi |

Semua APK sudah di-sign dengan 1 key yang sama (v3) dan sudah di-zipalign.

## Fitur yang terbuka
| Fitur | Sebelum | Sesudah |
|---|---|---|
| Sensitivity max | 1.4 (Free) | **5.0** (Elite) |
| Touch acceleration | terkunci (level > 0) | **aktif** |
| Target duration min | 5 ms | **1 ms** |
| Target interval min | 50 ms | **1 ms** |
| Indicator alpha | clamp min 0.5 | bebas |

## Patch yang dilakukan
1. `com/nebula/hnx/runtime/NebulaLicNative.smali` — `getLevel()` return `3`, `hasAccess()` return `true`
2. `com/pairip/application/Application.smali` — `LicenseClient.checkLicense()` dibuang (anti-tamper Play Integrity)
3. `stamp-cert-sha256` dihapus dari semua APK

## Cara install
1. Uninstall Nebula Touch versi Play Store (beda signature)
2. Install `NebulaTouch-1.2.6-VIP-MOD.apks` pakai app **SAI** (Split APKs Installer)
   — atau `adb install-multiple apk/*.apk`

> Catatan: tampilan tab Account masih membaca status dari Firestore (kosmetik), dan
> iklan AdMob masih aktif. Untuk pemakaian pribadi di perangkat sendiri.
