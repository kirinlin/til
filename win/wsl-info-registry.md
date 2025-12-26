# WSL infomation in registry

- Registry Path: `HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Lxss`
- Stored Information Includes:
    - DefaultDistribution (REG_SZ): GUID of the default WSL distribution launched when you run wsl.exe without arguments.
    - DefaultVersion (REG_DWORD): Indicates whether WSL1 or WSL2 is the default version.
    - BasePath (REG_SZ): Path to the distribution’s root filesystem on disk.
    - DistributionName (REG_SZ): Human-readable name of the distribution (e.g., Ubuntu).
    - DefaultUid (REG_DWORD): UID of the default user for the distribution.
    - Flags, State, Version: Internal values used by WSL to track distribution state and version.
    - NatIpAddress: IP address used by the host to access WSL networking

Not in registry:

Linux filesystems and user data (your `/home`, `/etc`, etc.) are stored in `ext4.vhdx`  files under `%LOCALAPPDATA%\Packages\<DistributionPackage>\LocalState`.
The registry only holds **metadata and configuration**, not the actual Linux environment contents.
