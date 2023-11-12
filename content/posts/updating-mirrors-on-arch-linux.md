+++
title = 'Updating Mirrors on Arch Linux'
date = 2023-11-12T17:44:46+05:30
+++

### What are Mirrors?

In Arch Linux, a mirror is a server that hosts packages i.e. bundled software for arch linux to be installed on your system, and these mirrors also keep updating these packages so that existing installations can upgrade to newer versions. Not all mirrors are always up, and not all mirorrs update the packages instantly. 

### Why Update Mirrors?

Keeping your mirrors updated is important for two reasons:

1. It ensures that your Arch Linux installation works correctly. If your mirrors are out of date, you might have trouble installing or updating software.

2. It can help you download software faster. If you're using a slow mirror, your downloads might be slow. By switching to a faster mirror, you can speed up your downloads.

### How to Update Mirrors

To update your mirrors, you'll need to use a tool called `reflector`. Here's a step-by-step guide:

1. **Install Reflector**: Reflector is a Python script that helps you update your mirrors. You can install it using the `pacman` package manager, which is the default package manager for Arch Linux. Run this command in your terminal to install reflector:

   ```bash
   sudo pacman -S reflector
   ```

2. **Update Mirrors**: After installing reflector, you can use it to update your mirrors. This is done by running the `reflector` command with a few options:

   ```bash
   sudo reflector --latest 20 --protocol https --sort rate --save /etc/pacman.d/mirrorlist
   ```

   Here's what each option does:

   - `--latest 20`: This tells reflector to get the 20 most recently synchronized mirrors.
   - `--protocol https`: This tells reflector to consider mirrors that use the HTTPS protocol.
   - `--sort rate`: This tells reflector to sort the mirrors by download speed.
   - `--save /etc/pacman.d/mirrorlist`: This tells reflector to save the selected mirrors to a file that `pacman` (the package manager) reads from [Source 0](https://kushagra-xo.github.io/thesillyscribbles/posts/updating-mirrors-on-arch-linux/).

### Automating Mirror Updates

You can also set up a timer to automatically update your mirrors once a week. This is done using the `systemd` system and service manager, which is the default for Arch Linux. Here's how to do it:

1. **Enable the Reflector Timer**: This tells `systemd` to start the reflector timer service when your computer boots up:

   ```bash
   sudo systemctl enable reflector.timer
   ```

2. **Start the Reflector Timer**: This starts the reflector timer service right away:

   ```bash
   sudo systemctl start reflector.timer
   ```

If you want to update your mirrors immediately, you can start the reflector service manually with this command:

```bash
sudo systemctl start reflector.service
```

### Read more:
- https://wiki.archlinux.org/title/Reflector
- https://wiki.archlinux.org/title/Mirrors
