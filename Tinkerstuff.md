https://forum.armbian.com/topic/5346-rtc-ds1307-i2c-for-tinkerboard/
Steps to use the ds3231 as system clock:

 

1) Add "echo ds1307 0x68 > /sys/class/i2c-adapter/i2c-1/new-device" to /etc/rc.local (if needed and above "exit 0")

2) In /lib/udev/hwclock-set comment out the following:

if [ -e /run/systemd/system ] ; then
    exit 0
fi

if [ -e /run/udev/hwclock-set ]; then
    exit 0
fi
then change the HCTOSYS_DEVICE=rtc0 to be HCTOSYS_DEVICE=rtc1

3)In /lib/udev/rules.d/50-udev-default.rules change the SUBSYSTEM=="rtc" line to:

SUBSYSTEM=="rtc", KERNEL=="rtc1", SYMLINK+="rtc", OPTIONS+="link_priority=-100"
4) In your hwclock udev rule make sure you have (/lib/udev/rules.d/85-hwclock.rules):

KERNEL=="rtc1", RUN+="/lib/udev/hwclock-set $root/$name"
