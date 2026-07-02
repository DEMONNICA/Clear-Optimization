> `Changelog:`
> - All significant changes to this project will be documented here.
---

> [8.0.0]
>
> - Added `Kokoro Mask`, `VortexSU` detection to `detect_root_all` in `customize.sh`.
> - Added fallback spoofed detection via `aapt` in `detect_root_all` in `customize.sh`.
> - Added `calc_total()` helper function with `bc` and `awk` fallback for size calculation.
> - Added `spinner()` animation during scan operations.
> - Added `sqlite3` availability check in option 5 — displays error and skips if not found.
> - Added `[!] No ... found.` message when scan result is empty — skips Y/N prompt.
> - Added 6 new optimization options to `cleaner`.
> - Added `[X]` as exit option to `cleaner`.
> - Added Y/N confirmation before every operation with total size and file count summary.
> - Added `Press Enter to continue...` prompt after each completed operation.
> - Added Y/N confirmation before every operation with total size and file count summary.
> - Added `Press Enter to continue...` prompt after each completed operation to prevent output overlap with menu.
> - Added `Deleting: <path>` with path in red, `Trimming: <partition>`, `Stopping: <package>`, and `Optimizing: <path>` output formats.
> - Changed FSTRIM — from manual remount loop across many partitions to `sm fstrim` + targeted loop on RW partitions only.
> - Changed Kill Apps — from verbose `Skipped: <pkg>` output to silent whitelist skip.
> - Changed `detect_root_all` detection order in `customize.sh` to APatch → KernelSU → Magisk.
> - Changed `detect_root_all` to use `for` loop with `pkg:label` pattern instead of chained `if/elif` blocks.
> - Changed APatch `.method` file to store 5 lines including `APATCH_APP_VER`.
> - Changed `.method` reading order in `service.sh` to APatch → KernelSU → Magisk.
> - Changed menu header from `Main Menu` to `System Optimization Menu`.
> - Changed deletion output format from `${R}Deleting: ${N}$file` to `${N}Deleting: ${R}${file}${N}` — path now highlighted in red.
> - Changed menu option format from `1. Option Name` to `[1] Option Name`.
> - Changed subtitle from generic description to `Clear Optimization — System Maintenance Tool`.
> - Removed option 9 `Clear RAM Cache`.
> - Removed option 1 `Clear Dalvik Cache`.
> - Removed option 2 `Remove System Dropbox Logs`.
> - Removed option 3 `Delete Temporary Files`.
> - Removed option 4 `Erase Tombstone Logs`.
> - Removed option 5 `Remove Empty Directories` — replaced by new option 2 with broader scope.
> - Removed option 6 `Clear Thumbnail Cache` — merged into option 4.
> - Removed option 7 `Clean System and Shader Cache` — merged into option 4.
> - Removed option 8 `FSTRIM` — replaced by new option 1 with `sm fstrim` support.
> - Removed option 9 `Clear RAM Cache`.
> - Removed `notify()` function and all notification calls.
> - Removed all numbered comments from `cleaner` — no longer needed in new structure.
---

> [7.0.0]
>
> - Added numbered comments to all sections in `verify.sh` (1–5) with sub-comments (3a/3b/3c for `verify_module_id`, 4a/4b/4c for `extract`).
> - Added numbered comments to all sections in `customize.sh` (1–12) with sub-comments (2a–2h for `detect_root_all`, 3a–3e for `device_info`, 6a–6c for `verify_module`, 9a–9b for `set_donate_link`).
> - Added numbered comments to all sections in `service.sh` (1–3).
> - Added numbered comments to all sections in `uninstall.sh` (1–4).
> - Added numbered comments and sub-comments to all options in `cleaner` (1–10 with sub-comments 1a/1b, 2a/2b, 3a–3c, 4a/4b, 5a/5b, 6a–6c, 7a–7c, 8a–8d, 9a–9c, 10a–10c) for options: Clear Dalvik Cache, Remove Dropbox Logs, Delete Temporary Files, Erase Tombstone Logs, Remove Empty Directories, Clear Thumbnail Cache, Clean System Cache, FSTRIM Optimization, Clear RAM Cache, Kill Third-Party Apps.
> - Added `ReSukiSU`, `WeaveMask`, `Kitsune Mask`, `FolkLite`, and `FolkPatch` detection to `detect_root_all` in `customize.sh`.
> - Added `ROOT_VERSION` extraction via `pm dump` for all KernelSU, Magisk, and APatch variants in `detect_root_all`.
> - Added SDK 37 (`Cinnamon Bun [C]`) to Android codename list in `device_info`.
> - Added `/proc/meminfo` fallback for RAM available calculation in `device_info`.
> - Added dynamic RAM label bucketing (2GB–32GB+) in `device_info`.
> - Added `until sys.boot_completed` wait loop in `service.sh`.
> - Added usage instructions for Termux in `README.md` TIP section — step-by-step guide for both `su` + `cleaner` and `su -c cleaner` methods.
> - Changed separate `display_current_time`, `display_device_info`, `display_ram_info`, and `check_android_version` functions into a single unified `device_info` function in `customize.sh`.
> - Changed Android codename format from `(Q)` to `[Q]` style in `device_info`.
> - Changed `detect_root_all` to use `DETECTED` flag and `return` after each root manager branch in `customize.sh`.
> - Changed license from GNU General Public License to Apache License 2.0.
> - Changed `BIN_FILES` variable inlined directly into `FILES` in `customize.sh` — removed separate variable.
> - Changed binary name from `CLEAR` to `cleaner` in `FILES` and `set_permissions` in `customize.sh`.
> - Changed banner image in `README.md` and `module.prop`.
> - Changed feature descriptions in `README.md` to reflect all updates — expanded feature 3, 5, 6, 7, 8, 9, and 10.
> - Changed root manager list in `README.md` TIP section to a concise format.
> - Changed cache cleanup loop in `uninstall.sh` to iterate directories directly using recursive `find`.
> - Changed shebang in `cleaner` from `#!/bin/sh` to `#!/system/bin/sh`.
> - Fixed `MODDIR` in `uninstall.sh` to use `readlink -f` for correct path resolution.
> - Fixed glob expansion in option 7 of `cleaner` — replaced variable-based glob with `find -maxdepth 3`.
> - Fixed thumbnail cleanup in option 6 of `cleaner` to delete all files inside thumbnail directories, not just specific extensions.
> - Removed `SKIPUNZIP=1` and `DEBUG=false` from `customize.sh`.
> - Removed `MODPATH` and `TMPDIR` fallback declarations from `customize.sh`.
> - Removed `icon()` function and asset extraction from `customize.sh`.
> - Removed icon cleanup loop (`/data/local/tmp/CLEAR*.png`) from `uninstall.sh`.
> - Removed `TMPDIR` fallback (`TMPDIR="${TMPDIR:-/data/local/tmp}"`) from `verify.sh`.
> - Removed `trap` cleanup in `verify.sh`.
> - Removed redundant `zip=$(clean_path "$zip")` inside `extract()` in `verify.sh`.
> - Removed `ANDROID_VERSION`, `ANDROID_SDK`, and `EMOT` block from `service.sh`.
> - Removed `sleep 10` from `service.sh`, replaced by `until sys.boot_completed` loop.
> - Removed `sed -i '[NEXT]'` version tag injection from `service.sh`.
> - Removed all system notification calls from `service.sh`.
> - Removed all `notify` calls from `cleaner`.
> - Removed `am kill-all` and `killall` from option 10 of `cleaner`, replaced by `am force-stop` only.
> - Removed unused `MODDIR` variable from `cleaner`.
---

> [6.6.6]
>
> - Changed option 10 to kill third-party apps.
> - Changed changelog structure, starting fresh for a cleaner and simpler format.
> - Changed some code to be more optimal and robust than the previous version.
---

> [5.0.0]
>
> - Added module banner for KernelSU Next.
> - Added root privilege check at startup — exits gracefully if not running with elevated permissions.
> - Added new optimization options: `9. Clear RAM Cache` using `drop_caches`, and `10. Execute All Optimizations` to run all tasks sequentially.
> - Added success notifications for each individual optimization and a comprehensive one for `All Optimizations`.
> - Added architecture check to support only `aarch64 (arm64-v8a)`, aborting installation on incompatible architectures.
> - Added `verify_module` function for strict checks on author, name, and ID format.
> - Changed user interface — removed vulgar language and adopted a cleaner, more professional tone throughout menu and messages.
> - Changed notification system to fall back to console output if `cmd notification` fails, and removed secondary icon argument for simplicity.
> - Changed cache cleaning in option 7 to include shader and GL cache files across `/data`, `/data/user_de`, `/storage/emulated/0/Android/data`, and `/cache`.
> - Changed filesystem trimming in option 8 — refined partition list to include `/persist` and `/apex`.
> - Changed thumbnail cache clearing in option 6 to target both `.thumbnail` and `.thumbnails` directories.
> - Changed deletion output to use `printf` consistently with colored logging, reducing unnecessary sleep delays.
> - Changed icon paths from `/data/media/0` to `/data/local/tmp` for better temporary file management.
> - Changed module ID handling to use `$ID="CLEAR"` for flexible path management in removal logic.
> - Changed root detection and version reporting in `service.sh` for accurate display in module description.
> - Changed external link in installation script from Trakteer to Telegram channel.
> - Changed Android codename handling — removed fallbacks and standardized for supported SDKs (29–36).
> - Changed error handling for Android SDK detection — aborts if version is invalid or undetectable.
> - Changed minimum Android version requirement to SDK 29 (Android 10).
> - Changed module version in `module.prop` to append `[FINAL]` tag for clear release identification.
> - Changed post-install notification message to guide users on running the module via Termux (`su -c CLEAR`).
> - Removed SDK 28 (`🦝`) support and adjusted emoji mapping to start from SDK 29.
> - Removed less common partitions like `/system_ext` and `/odm` from filesystem trimming for broader compatibility.
---

> [4.0.0]
>
> - Added option 8: Execute Deep FSTRIM on all supported partitions (`/data`, `/cache`, `/system`, `/system_ext`, `/product`, `/vendor`, `/odm`, `/oem`, `/metadata`, `/mnt`), with live status and error handling.
> - Changed shebang to `#!/bin/sh`.
> - Changed `service.sh` with minor code update.
> - Changed dalvik-cache cleanup to delete *all files* inside `/data/dalvik-cache/arm` and `/data/dalvik-cache/arm64`, not just `.dex` or `.vdex`, with real-time display.
> - Changed dropbox cleanup to delete all files inside `/data/system/dropbox` without removing the folders, with real-time display.
> - Changed junk file cleanup to remove files with extensions `.tmp`, `.bak`, `.old`, `.log`, and `.temp` recursively across all directories.
> - Changed tombstones cleanup to delete all files inside `/data/tombstones` and remove empty directories, with real-time display.
> - Changed empty directory cleanup to recursively delete empty directories under `/storage/emulated/0`, with real-time display.
> - Changed thumbnail cleanup to dynamically find all `.thumbnail` folders under `/storage/emulated/0` at any depth and delete files inside, with live display.
> - Changed cache cleanup to safely delete files only inside `cache` folders under `/storage/emulated/0/Android/data` and `/cache`, with real-time display.
> - Changed exit messages to be more forceful and consistent with the script style.
> - Changed all options to display file/folder deletion in real-time for transparency.
> - Changed menu option names for a more aggressive look and feel.
---

> [3.0.0]
>
> - Added `verify.sh` to automate the integrity check.
> - Added notification when removing selected options.
> - Added support for `armv8l` 32-bit.
> - Changed `module.prop` formatting.
> - Fixed `CLEAR` not working.
---

> [2.0.0]
>
> - Added `notify` function.
> - Changed output redirection handling in color variables.
> - Changed `find` command to use merged form.
> - Changed output format for better readability.
> - Changed `case` structure to be neater.
> - Changed other minor improvements.
---

> [1.0.0]
>
> - Initial release.
---