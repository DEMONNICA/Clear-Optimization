> <img width="3264" height="1836" alt="Image" src="https://github.com/user-attachments/assets/91aa834a-6930-4d82-8ca9-75162976165c" />

> [!NOTE]
> ```
> Optimize system performance by clearing unnecessary files and improving resource management.
> ```

> [!IMPORTANT]
> Features ✨:
> 1. Dalvik Cache Cleanup for clearing `/data/dalvik-cache/arm` and `/data/dalvik-cache/arm64` to optimize app performance.
> 2. System Dropbox Log Removal targeting `/data/system/dropbox` to eliminate unnecessary log files.
> 3. Temporary File Deletion scanning the entire system (excluding `/proc`, `/sys`, `/dev`, `/vendor`, `/data/data`, `/data/app`, and other critical paths) for files with temporary extensions such as `.tmp`, `.bak`, `.log`, `.old`, `.swp`, `.download`, `.partial`, `.temp`, `.dexopt`, and more.
> 4. Tombstone Log Erasure in `/data/tombstones` to remove crash logs and free up system resources.
> 5. Empty Directory Cleanup in `/storage/emulated/0` (excluding `/DCIM`, `/Android`, and `/Pictures`) to remove unused folders.
> 6. Thumbnail Cache Clearing targeting all thumbnail directories (`.thumbnails`, `.thumbnail`, `Thumbnails`, `.thumb`, `.thumbs`) across `/storage/emulated`, `/data/media`, `/sdcard`, and common app paths including DCIM, Pictures, WhatsApp, and Telegram.
> 7. System and Shader Cache Cleaning targeting cache, shader, and GL cache files in `/storage/emulated/0/Android/data`, `/cache`, `/data/user_de`, and app-level cache directories (`cache`, `code_cache`, `app_webview`) under `/data/data`.
> 8. FSTRIM Partition Optimization for trimming `/data`, `/cache`, `/system`, `/system_ext`, `/product`, `/vendor`, `/odm`, `/oem`, `/metadata`, and `/mnt` partitions to enhance I/O performance, with automatic read-write remount fallback for read-only partitions.
> 9. RAM Cache Clearing using `drop_caches` to free up memory and improve system responsiveness, with current value check to skip if already cleared.
> 10. Force Stop Third-Party Apps using `am force-stop` to kill all non-system apps except whitelisted ones (Termux), ensuring system packages are never affected.

> [!TIP]
> 1. Supports `Magisk` `KernelSU` `KernelSU Next` `APatch` `SukiSU` and their variants.
> 2. Minimum Android `10 SDK 29`.
> 3. To run the module, open **Termux** and follow the steps below:
>    - **Method 1** — Enter root shell first, then launch the tool:
>      ```sh
>      su
>      ```
>      After pressing **Enter**, your prompt will change to `#`, meaning you are now in root mode. Then type:
>      ```sh
>      cleaner
>      ```
>      Press **Enter** to launch the optimization menu.
>    - **Method 2** — Run directly in a single command:
>      ```sh
>      su -c cleaner
>      ```
>    > Both methods require root access. A root manager such as Magisk, KernelSU, or APatch must be installed on your device.
> 4. If `cleaner` command is not found, install **Meta** to enable system binary overlay support:
>    - [Download Meta — Hybrid Mount](https://github.com/Hybrid-Mount/meta-hybrid_mount/releases)
> 5. If `cleaner` is still not accessible after installing Meta, run it directly via full path:
>    ```sh
>    su -c /data/adb/modules/CLEAR/system/bin/cleaner
>    ```

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

> Download 📦:
> - [Download now Clear Optimization.](https://shrinkme.click/4wdMx)
> - [For Magisk Modules or other Plugins, please visit here.](https://t.me/Demoniica)
----