Tweaks done on RPI3 

1 Install Zram 

 sudo apt-get install zram-config
 
 2. Configure bluetooth
 
 3.Fix date time
 
 - Run: sudo apt-get ntp
- Run: sudo apt-get ntpdate
- To sync time: sudo ntpdate-debian or sudo ntpdate server 1.us.pool.ntp.org
- To view a date stamp run: date

 
 https://github.com/rlancaste/AstroPi3
 
 https://github.com/rkaczorek/astroberry-server/
 
To disable powermanagement

Run : iwconfig

sudo nano  /etc/network/interfaces 

add line: wireless-power off


https://www.raspberrypi.org/forums/viewtopic.php?f=36&t=167510
https://www.tinkerboarding.co.uk/forum/showthread.php?tid=66
