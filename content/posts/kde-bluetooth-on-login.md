+++
title = 'Kde Bluetooth Disabled on Login'
date = 2023-10-13T13:03:03+05:30
+++

Lately i had been dealing with an issue where my bluetooth would disable automatically upon login. I had done a lot of troubleshooting to realize that the issue was with me *abruptly rebooting* instead of rebooting via the gui.

Which would cause `~/.config/bluedevilglobalrc` to look something like this:
```
[Adapters]
44:85:00:80:3C:BA_powered=false
```

## Solution:

### 1. Comment out the line to look something like this:

```
[Adapters]
#44:85:00:80:3C:BA_powered=false
```
I have tested this and there does not seem to be any functionality issue whatsoever

### 2. Make the file read-only or immutable

- Change the file to look like this:
```
[Adapters]
44:85:00:80:3C:BA_powered=true
```

```bash 
$ chattr +i ~/.config/bluedevilglobalrc
```

### 3. Only use GUI reboot

## References:

- https://www.reddit.com/r/ManjaroLinux/comments/12fgj3o/kde_plasma_bluetooth_not_automatically_powered_on/
- https://bugs.kde.org/show_bug.cgi?id=469119
