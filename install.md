the docs just have

`pacstrap -K /mnt base linux linux-firmware`

but you should do

`pacstrap -K /mnt base linux linux-firmware micro amd-ucode`

* Gives you a text editor whne finishing the install
* Gives you microcode updates for when you are configuring your kernel boot flags

