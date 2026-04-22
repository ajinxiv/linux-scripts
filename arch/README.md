# arch

some scripts i use in my arch linux installation

## scripts

### `update-all`

updates the system and packages (pacman) and flatpak
apps, if present.

it basically runs `sudo pacman -Syu` and
`flatpak update -y` (if present).

> ![NOTE]
> this script is not meant to be run as sudo.
> it will fail if run in sudo mode.

usage:

```bash
$ update-all
```

