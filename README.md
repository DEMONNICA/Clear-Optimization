> ![Image](https://github.com/user-attachments/assets/ca003a2c-a420-4fca-920a-6154c5d502ac)

> [!NOTE]
> ```
> Optimizes GPS performance and stability by configuring system GPS files, applying targeted properties, and granting location permissions on every reboot.
> ```

> [!IMPORTANT]
> Features ✨:
> 1. Writes optimized `gps.conf`, `gnss.conf`, `flp.conf`, and `gps.xml` on every boot.
> 2. Enables multi-satellite support via `GPS`, `GLONASS`, `BeiDou`, `Galileo`, `QZSS`, and `SBAS`.
> 3. Configures `SUPL`, `XTRA`, and `NTP` servers for faster assisted fix.
> 4. Applies `persist.sys.gps.lpp` via `resetprop` only if present on the device.
> 5. Activates high accuracy location mode and all location providers on every boot.
> 6. Grants location permissions to `Google Play Services` and `Google Maps`.
> 7. Broadcasts `android.location.PROVIDERS_CHANGED` to reload location providers after config apply.
> 8. Backs up original GPS config files and restores them automatically on uninstall.

> [!TIP]
> 1. Supports `Magisk` `KernelSU` `KernelSU Next` `APatch` `SukiSU` and their variants.
> 2. Minimum Android `10 SDK 29`.
> 3. This module modifies files in `system/vendor/etc`. For proper system file overlay support, it is recommended to use **Meta — Hybrid Mount**:
>    - [Download Meta — Hybrid Mount](https://github.com/Hybrid-Mount/meta-hybrid_mount/releases)

> [!WARNING]
> Disclaimers 🛡️:
> - Use at your own risk. No guarantees are made regarding stability, compatibility, or safety. Always back up your data before installing anything.
> - These works are tested on specific devices only. Behavior on other devices may vary significantly.
> - The author reserves the right to discontinue, modify, or remove any module or plugin at any time without prior notice.

> [!CAUTION]
> Warning ☢️:
> 1. The developer takes no responsibility for any damage, data loss, or device malfunction caused by the use of these works.
> 2. System modifications can be unpredictable. What works on one device may break another.
> 3. Always have a recovery solution ready — TWRP, ADB, or fastboot — before proceeding.
> 4. If you do not fully understand what a modification does, do not apply it.
> 5. Redistribution, modification, or repackaging of these works without explicit permission from the author is strictly prohibited.
> 6. Rooted devices with custom ROM may behave differently. Proceed with extra caution.
> 7. Any modification applied to the system is your decision. Think before you act.