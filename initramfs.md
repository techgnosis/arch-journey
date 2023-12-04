initrd vs initramfs. initramfs is the only option today. the flag still says initrd and sometimes the file is called initrd but its all initramfs, which is a compressed cpio archive

initramfs is also referred to as "early userspace"

mkinitcpio \
--config /etc/mkinitcpio.conf
--kernel 6.6.2-arch1-1 \
--generate path_to_new_img


in Arch its a zstd compressed cpio archive

file starts off as .img
file says its a zstd file
mv file.img file.zst
unzstd file.zst

This generates a cpio archive that is the same size on disk as the one that Arch generated for me during install!

cpio --extract --file file
that will unpack to current directory
its a file system, as expected