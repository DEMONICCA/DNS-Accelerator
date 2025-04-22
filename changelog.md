# Changelog

> All significant changes to this project will be documented here.

---

> [2.0.0]
>
> - Total update to the `customize.sh` section
> - Add `verify.sh` to automate the `integrity` check.
> - Major rewrite and optimization of `DNS` and `service.sh` scripts.
> - Improved root method detection with clean fallback (`KernelSU`, `Magisk`, `APatch`, and unknown).
> - Rewritten `module.prop` updater with emoji by Android SDK and full compatibility handling.
> - Enhanced DNS configuration with dynamic system property update per interface.
> - Prevents duplicate iptables rules with built-in check before adding.
> - Removed background infinite loop for DNS flushing (replaced with a one-time conditional flush).
> - Removed all potentially unsafe file deletions (`rm -rf`).
> - Ensured SELinux state is restored after script execution.
> - Added uninstall support via `uninstall.sh`:
>   - Resets all modified `sysctl` parameters to system default.
>   - Cleans up DNS properties across all interfaces.
>   - Removes iptables NAT DNS redirection rules.
>   - Deletes module-created `resolv.conf`
---

> [1.5.0]
>
> - Fixing `module.prop` description that has piled up when it reboots several times.
> - Simplified the code in `service.sh` for compatible modules.
---

> [1.0.0]
>
> - Initial release.
> - Version `1.0.0` uses Cloudflare DNS `1.1.1.1` and `1.0.0.1`
> - Implemented root detection and version information fetching.
> - Automatic updating of `module.prop` file with root and Android data.
> - Implementation of optimal network and DNS settings.
> - Increased TX power for network connectivity.
> - Automatic system cache clearing and DNS flush.
> - Temporary disabling of SELinux during configuration.
---
