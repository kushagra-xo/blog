+++
title = 'Updating Mirrors on Arch Linux'
date = 2023-11-12T17:44:46+05:30
+++

Having up-to-date mirrors and working mirrors is crucial in an archlinux
installation to ensure correct pacman functionality i.e. everything updates
as it should and optimal download speeds.

The recommended tool for this task is
[reflector](https://wiki.archlinux.org/title/reflector), a Python script that
retrieves the latest mirror list from the MirrorStatus page, filters and sorts
them by speed (when the correct flags are used), and overwrites the
`/etc/pacman.d/mirrorlist`(pacman reads mirrors from this here) file.

## Install reflector

```bash
sudo pacman -S reflector
```

## Update mirrors

```bash
sudo reflector --latest 20 --protocol https --sort rate --save /etc/pacman.d/mirrorlist
```

- --latest 50: This option tells reflector to retrieve the 50 most recently
synchronized mirrors.
- --protocol https: This option tells reflector to consider both HTTP and HTTPS protocols.
- --sort rate: This option tells reflector to sort the mirrors by download speed.
- --save /etc/pacman.d/mirrorlist: This option tells reflector to save the
selected mirrors to the /etc/pacman.d/mirrorlist file.

## Automate

To automate the mirror updating process, you can use the reflector.timer
systemd unit:

```bash
sudo systemctl enable reflector.timer
sudo systemctl start reflector.timer
```

By default, it will start reflector.service once a week. If you want
to update the mirror list immediately, you can start reflector.service manually:

```bash
sudo systemctl start reflector.service
```

### Read more:

- https://wiki.archlinux.org/title/Reflector
- https://man.archlinux.org/man/reflector.1#EXAMPLES
- https://wiki.archlinux.org/title/Mirrors
- https://wiki.archlinux.org/title/Pacman
