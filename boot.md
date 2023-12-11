Don't rely on a bootloader. You can edit the UEFI Boot Manager settings directly with `efibootmgr` and boot directly into Arch

You can also do this with a tool called `UEFI Shell` which you can boot into from the Arch ISO, but that is a bit harder since you don't have access to `/dev` filesystem that has all your disk IDs. 

If you boot into UEFI Shell, you can run the kernel as an executable since it is built as a "UEFI Application" using EFISTUB
https://wiki.archlinux.org/title/EFISTUB

`efibootmgr --create --disk /dev/disk/by-id/xxx --part 2 --label "Arch" --loader vmlinuz --unicode ' root=/dev/sda3 initrd=\efi\boot\initramfs.img'`

* There MUST be a space in front of the --unicode string
* Do NOT set `root=` to a traditional alphanumeric ID like `/dev/sda2` as those can change and you might boot into the wrong OS

`efibootmgr -b 000x -B`


https://docs.kernel.org/admin-guide/efi-stub.html

`fwupd` can update UEFI


Coreboot can run Tianocore as a payload. So that means Tianocore provides all the interfaces in the UEFI specification but Tianocore in this case would not interface with the hardware. Tianocore implements all the interfaces via coreboot. I think?

