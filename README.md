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

https://raspberrypi.stackexchange.com/questions/15944/can-i-directly-connect-to-my-pi-wirelessly-without-a-router

https://thepi.io/how-to-use-your-raspberry-pi-as-a-wireless-access-point/

http://raspberry-at-home.com/hotspot-wifi-access-point/


https://lcdev.dk/2012/11/18/raspberry-pi-tutorial-connect-to-wifi-or-create-an-encrypted-dhcp-enabled-ad-hoc-network-as-fallback/#comment-640

https://superuser.com/questions/1130195/linux-make-hotspot-without-bridging-internet-access-with-secondary-usb-wi-fi-d


https://github.com/ulno/create_ap
