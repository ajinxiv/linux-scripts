# arch

some scripts i use in my arch linux installation

## scripts

### `full-update`

updates the system and packages (pacman) and flatpak
apps, if present.

it basically runs `sudo pacman -Syu` and
`flatpak update -y` (if present).

> ![NOTE]
> this script is not meant to be run as sudo.
> it will fail if run in sudo mode.

usage:

```bash
$ full-update
```

### `quick-setup`

sets up various system optimizations and settings.

this script:
- increases system responsiveness:
    - tunes graphics drivers for Radeon GPUs
    - tunes ROCm to work on Radeon RX 6600
    - creates a 4GB max Z-Ram
    - enables and configures resolved to cache DNS
    - increases network backlog
    - tunes schedulers for storage device types
    - tunes reduces audio latency problems
    - loads NTSync for better performance in Windows software
- customizes the system:
    - adds custom bashrc for skel
    - adds ~/.local/bin to PATH on system level
    - enables password feedback for SUDO
    - sets up wheel group for admins
    - configures iommu for pass-through
    - configures system resolution to 1920x1080 @ 200Hz
- improves sytem usability:
    - loads I2C-dev to allow changing monitor brightness via DDCutil

usage:

```bash
# quick-setup
```
