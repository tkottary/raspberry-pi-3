### Pre requistes:
* Synscan or SynScan Pro app on iOS or Android Device.
* Skywatcher AZGTI
* Laptop/Desktop/Raspberry Pi(SBC) with Kstars& Indi.
 
1. Start the mount , you should see red light blinking and wifi signal with synscan_XXXX)

2. Connect the device to mount wifi. 
 * Open the app  connect in EQ mode .
 * Do 1 star alignment or press up/down/left/right buttons on the app to see if the mount responds to  App commands.  
 * Your device should most likely get 192.168.4.2 as the IP Address. 
 * SynScan recommends to keep the app open all times, so turn off display going to sleep on this device.
 
3. Connect your Laptop/Desktop/RPI to Mount wifi (SynScan). 

4. Launch Kstars and choose SynScan as the indi mount driver.
![Indi Mount Driver](https://github.com/tkottary/raspberry-pi-3/blob/master/kstars1.jpg)

5. Configure the connection options  as below.
Connection mode as Ethernet
IP address to 192.168.4.2 ( IP address of the device having synscan app)
Port 11882
Connection Type to TCP
![Ekos Connection Setting](https://github.com/tkottary/raspberry-pi-3/blob/master/kstars2.jpg)

Connect and Enjoy the mount
