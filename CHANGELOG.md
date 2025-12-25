> `Changelog:`
> - All significant changes to this project will be documented here.
---

> [6.0.0] `THE FINAL END`
>
> - Changed the module banner and added a new function `uninstall.sh`
> - Refactored cleanup logic for improved readability and structured execution.
> - Improved safety by excluding critical processes and system components from termination.
> - Enhanced cache cleanup coverage across application, system, and runtime directories.
> - Optimized process termination logic to reduce redundant kill attempts.
> - Improved compatibility across different Android versions and runtime environments.
> - Reduced risk of unintended system instability during cleanup operations.
> - Streamlined execution flow for faster and more deterministic cleanup behavior.
> - This version replaces the previous implementation with a safer and more maintainable approach.
> - Improved compatibility across KernelSU, Magisk, and APatch environments.
> - Enhanced safety by protecting critical system components during cleanup.
> - Refined root detection and Android version validation for better reliability.
> - Updated runtime notifications and module metadata for clearer user feedback.
> - Improved overall stability, performance, and maintainability.
---

> [5.0.0] `FINAL`
>
> - Introduced module banner for KernelSU Next.
> - Refined user interface by removing vulgar language and adopting a clean, professional tone throughout the menu and messages.
> - Added root privilege check at startup to ensure the script runs only with elevated permissions, exiting gracefully if not.
> - Introduced new optimization options: "9. Clear RAM Cache" using `drop_caches` for memory management, and "10. Execute All Optimizations" to run all tasks sequentially.
> - Enhanced notification system with error handling, falling back to console output if `cmd notification` fails, and removed secondary icon argument for simplicity.
> - Expanded cache cleaning in option 7 to include shader and GL cache files across `/data`, `/data/user_de`, `/storage/emulated/0/Android/data`, and `/cache`.
> - Optimized filesystem trimming (option 8) by refining partition list to include `/persist` and `/apex`, while removing less common ones like `/system_ext` and `/odm` for broader compatibility.
> - Improved thumbnail cache clearing (option 6) to target both `.thumbnail` and `.thumbnails` directories for more comprehensive cleanup.
> - Streamlined deletion output by using `printf` consistently with colored logging, reducing unnecessary sleep delays for faster execution.
> - Updated icon paths from `/data/media/0` to `/data/local/tmp` for better temporary file management.
> - Added success notifications for each individual optimization and a comprehensive one for "All Optimizations".
> - Minor tweaks to menu display, including ASCII art adjustments and standardized formatting for improved readability.
> - Raised minimum Android version requirement to SDK 29 (Android 10), removing support for SDK 28 to align with modern devices.
> - Introduced architecture check to support only aarch64 (arm64-v8a), aborting installation on incompatible architectures.
> - Implemented dynamic module ID handling with `$ID="CLEAR"` for flexible path management in removal logic.
> - Enhanced module verification with new `verify_module` function, enforcing strict checks on author, name, and ID format.
> - Updated icon extraction paths to `/data/local/tmp` for better temporary file handling and consistency.
> - Refined root detection and version reporting in `service.sh` for accurate display in module description.
> - Removed SDK 28 emoji (`🦝`) and adjusted emoji mapping to start from SDK 29 in module description.
> - Appended `[FINAL]` tag to module version in `module.prop` for clear release identification.
> - Improved post-install notification message to guide users on running the module via Termux (`su -c CLEAR`).
> - Changed external link in installation script from Trakteer to Telegram channel for updated community access.
> - Optimized Android codename handling, removing fallbacks and standardizing for supported SDKs (29–36).
> - Streamlined error handling for Android SDK detection, aborting if version is invalid or undetectable.
> - Minor UI print message improvements for clarity during module detection and removal.
> - Other small optimizations for installation efficiency and script maintainability.
> - And there are many more optimization changes and updates that I didn't mention.
---

> [4.0.0]
>
> - Minor code update to `service.sh`.
> - Changed shebang to `#!/bin/sh`.
> - Now deletes *all files* inside `/data/dalvik-cache/arm` and `/data/dalvik-cache/arm64`, not just `.dex` or `.vdex`, and displays each deleted file in real-time.
> - Deletes all files inside `/data/system/dropbox` without removing the folders, displaying deleted files in real-time.
> - Removes files with extensions `.tmp`, `.bak`, `.old`, `.log`, and `.temp` recursively across all directories.
> - Deletes all files inside `/data/tombstones` and removes empty directories, showing deleted files and folders in real-time.
> - Recursively deletes empty directories under `/storage/emulated/0`, displaying removed folders in real-time.
> - Dynamically finds all `.thumbnail` folders under `/storage/emulated/0` at any depth, deletes files inside (not folders), and shows deleted files live.
> - Refined to safely delete files only inside `cache` folders under `/storage/emulated/0/Android/data` and `/cache`, with real-time deletion display.
> - Added option 8: Execute Deep FSTRIM on all supported partitions (`/data`, `/cache`, `/system`, `/system_ext`, `/product`, `/vendor`, `/odm`, `/oem`, `/metadata`, `/mnt`), with live status and error handling.
> - Updated exit messages to be more forceful and consistent with the script style.
> - All options now display file/folder deletion in real-time for transparency.
> - Notification function remains active to notify the system after each cleanup.
> - Menu option names strengthened for a more aggressive look and feel.
___

> [3.0.0]
>
> - Add `verify.sh` to automate the `integrity` check.
> - Supports `armv8l` 32bit.
> - Fixed `CLEAR` not working.
> - Adding notification is complete.
> - Beautifying module.prop.
> - Update notification when removing selected options.
___

> [2.0.0]
>
> - Removal of Output Redirection in Color Variables.
> - Notify function creation.
> - Merge Find command.
> - Improved Output Format.
> - Neater Case Structure.
> - And other minor improvements.
---

> [1.0.0]
>
> - Initial release.
---