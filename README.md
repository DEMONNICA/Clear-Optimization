> <img width="3264" height="1836" alt="Image" src="https://github.com/user-attachments/assets/91aa834a-6930-4d82-8ca9-75162976165c" />

> [!NOTE]
> ```
> Optimize system performance by clearing unnecessary files and improving resource management.
> ```

> [!IMPORTANT]
> Features ✨:
> 1. FSTRIM Partition Optimization for trimming system partitions to enhance I/O performance.
> 2. Empty Directory Cleanup to remove unused empty folders from internal storage.
> 3. Application Cache Cleanup targeting cache directories and files across app data storage.
> 4. System Junk Cleanup removing temporary files, thumbnail cache, compiled artifacts, system logs, recent tasks, and other system junk.
> 5. Database Optimization running WAL checkpoint and VACUUM on all application databases to improve read performance and reduce file size.
> 6. Kill Background Apps to terminate all third-party background applications, with Termux excluded from the process.

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