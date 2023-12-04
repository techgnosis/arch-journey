Don't rely on a bootloader. You can edit the UEFI Boot Manager settings directly with `efibootmgr` and boot directly into Arch

You can also do this with a tool called `UEFI Shell` which you can boot into from the Arch ISO, but that is a bit harder since you don't have access to `/dev` filesystem that has all your disk IDs.


`efibootmgr --create --disk /dev/disk/by-id/xxx --part 2 --label "Arch" --loader vmlinuz --unicode ' root=/dev/sda3 initrd=\efi\boot\initramfs.img'`

* There MUST be a space in front of the --unicode string
* Do NOT set `root=` to a traditional alphanumeric ID like `/dev/sda2` as those can change and you might boot into the wrong OS

`efibootmgr -b 000x -B`

