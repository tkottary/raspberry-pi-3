###### 1 . Run this to remove modemanager

sudo apt-get remove modemmanager

###### 2 .Pair your bluetooth device with linux mosly using blueman

Make sure  blueman does not autoconnect upon reboot


###### 3.Find the macaddress of the bluetooth device and replace it in the below script.

To get mac address of bluetooth run below on console.

sudo hciconfig

#### copy this to text file and save it as Bluetooth-EQmod.sh

```
#!/bin/bash

sudo rfcomm bind hci0 XX:XX:XX:XX:XX:XX 1 &
sleep 5
sudo chown astroberry /dev/rfcomm0

```

######  4 Now run the attached script by 

    replacing XX:XX:XX:XX:XX:XX  with your mac address.
    replace astroberry with your desktop username

Then run below on console.

sudo chmod 755 Bluetooth-EQmod.sh

sh Bluetooth-EQmod.sh


###### 5. After this , consequent reboot you can just run 

sh Bluetooth-EQmod.sh



######  # To automatically Run it

add this line to end of file /etc/rc.local (replace xx with mac address)

rfcomm bind hci0 XX:XX:XX:XX:XX:XX 1 &
