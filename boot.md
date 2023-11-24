Do all the work in UEFI Shell

You can boot into UEFI Shell from the Arch ISO

I can use the `bcfg` command to edit the list
`bcfg boot dump -v`
`bcfg boot rm 01`
I can use `bcfg boot add 01`


Use `bcfg boot addp` when adding an entry that lives on a USB stick


Super sweet, I don't have to install a bootloader of any kind. I can do one of the following:
1. Boot Arch manually from the UEFI shell on the Arch ISO
2. I can manually add a boot entry for Arch using the UEFI shell

The `edit` command in UEFI shell uses `F2` as save and `F3` to quit

`edit fs1:\options.txt`

`bcfg boot -opt 0x? fs1:\options.txt`

THERE MUST BE A SPACE IN FRONT OF THIS LINE IN options.txt

` root=/dev/sda2 initrd=initramfs-linux.img`

Microcode needs to be added via a second initrd flag

` root=/dev/sda2 initrd=intel-ucode.img initrd=initramfs-linux.img`



https://wiki.archlinux.org/title/EFISTUB#UEFI_Shell
https://wiki.archlinux.org/title/Unified_Extensible_Firmware_Interface#Important_UEFI_Shell_commands
https://www.digitalstorm.com/forums/howto-add-uefi-shell-boot-option-tidf53003/
https://superuser.com/questions/1035522/how-to-add-booting-parameters-to-the-kernel-with-bcfg-from-the-efi-shell

