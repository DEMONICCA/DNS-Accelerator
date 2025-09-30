> `Changelog:`
> - All significant changes to this project will be documented here.
---

> [3.0.0]
>
> - Introduced module banner for KernelSU Next.
> - Renamed `print_time` to `display_current_time` and `print_device` to `display_device_info` in `customize.sh` for clearer function naming.
> - Added `display_ram_info` function in `customize.sh` to show RAM usage details during installation.
> - Introduced `module_remove_check` with dynamic `ID="DNS"` in `customize.sh` for more flexible module removal.
> - Raised minimum Android version requirement from SDK 28 (Pie) to SDK 29 (Q) in `customize.sh` for better compatibility.
> - Added `verify_module` function in `customize.sh` to validate module ID and author in `module.prop`.
> - Optimized icon extraction in `customize.sh` by moving `dns_accelarator_*.png` to `/data/local/tmp` for consistency.
> - Updated `print_random_devil_message` in `customize.sh` with revised devil-themed messages and consistent naming.
> - Enhanced `service.sh` with improved root detection logic, including version details for Magisk, KernelSU, and APatch.
> - Modified `module.prop` description in `service.sh` to include emoji-based Android SDK indicators and remove `FIX` suffix.
> - Added PID tracking in `service.sh` by saving `DNS` process ID to `DNS.pid` and updating `module.prop` with PID info.
> - Streamlined `uninstall.sh` by consolidating cache cleanup (`code_cache`, `shader`, `glcache`, `cache`) into a single `find` command.
> - Expanded `SYSCTL_PARAMS` in `uninstall.sh` to reset all modified network parameters to their defaults.
> - Improved `uninstall.sh` by restoring `private_dns_mode` to `opportunistic` for Android 10 (SDK 29).
> - Updated `DNS` script to use `write_config` function for consistent file writing and permission setting.
> - Adjusted `DNS` notification to use `Accelarator_*.png` icons from `/data/local/tmp` and improved message clarity.
> - Enhanced `verify.sh` with SHA-512 support alongside SHA-256 for stronger file integrity checks.
> - Optimized `set_dns_properties` in `DNS` to skip redundant DNS updates and improve performance.
> - Removed verbose cleanup logging in `uninstall.sh` for a cleaner uninstall process.
> - Fixed `DNS` script to handle Android SDK 29 private DNS settings more robustly with fallback options.
> - Updated post-install notification in `customize.sh` to include reboot prompt for clarity.
> - Minor bug fixes and performance optimizations across all scripts.
---

> [2.0.0]
>
> - Total update to the `customize.sh` section.
> - Add `verify.sh` to automate the `integrity` check.
> - Major rewrite and optimization of `DNS` and `service.sh` scripts.
> - Improved root method detection with clean fallback (`KernelSU`, `Magisk`, `APatch`, and unknown).
> - Rewritten `module.prop` updater with emoji by Android SDK and full compatibility handling.
> - Enhanced DNS configuration with dynamic system property update per interface.
> - Prevents duplicate iptables rules with built-in check before adding.
> - Removed background infinite loop for DNS flushing (replaced with a one-time conditional flush).
> - Removed all potentially unsafe file deletions (`rm -rf`).
> - Ensured SELinux state is restored after script execution.
> - Added uninstall support via `uninstall.sh`.
> - Resets all modified `sysctl` parameters to system default.
> - Cleans up DNS properties across all interfaces.
> - Removes iptables NAT DNS redirection rules.
> - Deletes module-created `resolv.conf`
---

> [1.5.0]
>
> - Fixing `module.prop` description that has piled up when it reboots several times.
> - Simplified the code in `service.sh` for compatible modules.
---

> [1.0.0]
>
> - Initial release.
> - Version `1.0.0` uses Cloudflare DNS `1.1.1.1` and `1.0.0.1`.
> - Implemented root detection and version information fetching.
> - Automatic updating of `module.prop` file with root and Android data.
> - Implementation of optimal network and DNS settings.
> - Increased TX power for network connectivity.
> - Automatic system cache clearing and DNS flush.
> - Temporary disabling of SELinux during configuration.
---