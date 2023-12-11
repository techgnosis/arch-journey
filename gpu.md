Need to pass this to kernel as commandline parameter
`amdgpu.ppfeaturemask=0xffffffff"`
You can check `/proc/cmdline` to see what was passed to the kernel

This is what worked for me. Setting the maximum wattage
`echo 100000000 > /sys/class/drm/card0/device/hwmon/hwmon0/power1_cap`
The default is 135000000 and is measured in micro watts


I think sclk is "system clock" and mclk is "memory clock"

pp is "power play" which is the brand name for their clock management. everything starts with pp


CoreCtl seems like a good GUI
https://gitlab.com/corectrl/corectrl

https://docs.kernel.org/gpu/amdgpu/thermal.html
https://community.amd.com/t5/graphics-cards/rx-580-black-screen-crash-after-playing-for-30-60-minutes/m-p/517556
https://unix.stackexchange.com/questions/620072/reduce-amd-gpu-wattage
https://wiki.archlinux.org/title/AMDGPU
