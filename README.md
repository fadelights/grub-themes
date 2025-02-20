# grub-themes
Collection of GRUB themes I acquired from around the internet and modified to my liking.

## Usage

1. Choose the folder of a theme you like and copy the entire directory to `/boot/grub2/themes/` -- this is the
   default themes directory for openSUSE, but you don't need to strictly adhere to it. You can place the themes
   anywhere.
1. Update your GRUB settings located at `/etc/default/grub` and change the value of `GRUB_THEME` to the location
   of the `theme.txt` file for your chosen theme. For example:
   ```
   GRUB_THEME=/boot/grub2/themes/cyberGRUB/theme.txt
   ```
1. Run `update-grub`. If you don't have it, you can instead create it in `/usr/sbin/update-grub` and set
   the contents to the following:
   ```
   #!/bin/sh
   set -e
   exec grub2-mkconfig -o /boot/grub2/grub.cfg "$@"
   ```
1. Reboot.
