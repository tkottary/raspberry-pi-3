##### Tweaks done on RPI3 

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

https://adamscheller.com/systems-administration/rtl8192cu-fix-wifi/
 

4 To start VNC for RPI3 or tinker

sudo apt-get -y install novnc tightvncserver
cd ~
mkdir .config;cd .config
mkdir autostart;cd autostart
nano tightvnc.desktop

[Desktop Entry]
Type=Application
Name=TightVNC
Exec=vncserver :1
StartupNotify=false
save and reboot

Ref : https://learn.adafruit.com/adafruit-raspberry-pi-lesson-7-remote-control-with-vnc/running-vncserver-at-startup

Fix mouse issue on Tinkerboard /Ubuntu xenail

xset m 1/2 4


sudo apt install tightvncserver
sudo apt-get install xfonts-75dpi
sudo apt-get install xfonts-100dpi
sudo apt-get install xfonts-base
run tightvncserver, set password, connect with whatever vnc client you want.


sudo nano /etc/rc.local

#add a line of su – tkoy -c ‘/usr/bin/tightvncserver :1’


#assign static ip to RPi3 to connect via Ethernet port directly

Configure a static network adddress on your Pi in /etc/network/interfaces

auto eth0
iface eth0 inet static
        address 10.1.1.30
        netmask 255.255.255.0
        gateway 10.1.1.1
        
        (gateway was kept same in windows 10 as well) for the 2nd ethernet port.
        
        
