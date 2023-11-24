First attempt did not work. I do not see Arch in my boot menu.

There have been weird entries in my UEFI boot menu for a while. I want to clear them out.
Opened up UEFI Shell

I can use the `bcfg` command to edit the list
`bcfg boot dump -v`
`bcfg boot rm 01`
I can use `bcfg boot add 01`


Use `bcfg boot addp` when adding an entry that lives on a USB stick


Super sweet, I don't have to install a bootloader of any kind. I can do one of the following:
1. Boot Arch manually from the UEFI shell on the Arch ISO
2. I can manually add a boot entry for Arch using the UEFI shell


THERE MUST BE A SPACE IN FRONT OF THIS LINE IN options.txt
` root=/dev/sda2 initrd=initramfs-linux.img`


https://wiki.archlinux.org/title/EFISTUB#UEFI_Shell
https://wiki.archlinux.org/title/Unified_Extensible_Firmware_Interface#Important_UEFI_Shell_commands
https://www.digitalstorm.com/forums/howto-add-uefi-shell-boot-option-tidf53003/
https://superuser.com/questions/1035522/how-to-add-booting-parameters-to-the-kernel-with-bcfg-from-the-efi-shell

