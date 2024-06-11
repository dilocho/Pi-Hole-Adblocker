# Pi-Hole-Adblocker

## Objective

To enable a ad blocker on all devices in a home network using Pi-Hole. 

### Tools Used
Hardware: 
- Rapsberry Pi 

Software: 
- Pi-hole
- PuTTY

## Steps
Before setting up Ad Blocker I had to install the software through my laptop on the SD card using Imager. Once completed I used PuTTY to remote access into the device for intial set up with my home network and update and install Pi-Hole using the curl function.  

1. Configured router to provide a static IP address to device on router settings 
        a) Log into router 
        b) Advanced settings > DHCP
        c) Found the IP and MAC address for RaspberryPi 
        d) Reserved the IP address to the router and applied changes 
        e) Defaulted as 192.168.0.217

![image](https://github.com/dilocho/Pi-Hole-Adblocker/assets/38048735/554e6814-67db-45c2-a83f-47b7d79ac4a9) 

*Ref 1. Intial set up assigning local address and number of CPE's*

2. Since there is no way to direct my particular hub to a DNS. The other alternative would be to set up the DHCP to point to only one IP and change the CPE’s to 1 (directed at the rapsberry pi).

![image](https://github.com/dilocho/Pi-Hole-Adblocker/assets/38048735/ecd52d38-210e-4889-a03a-2c7fe17dcf61)
*Ref 2. Disabling DHCP and allowing Pi Hole to become the default DHCP server*

3. To view your dashboard go to "IP ADDRESS/admin"

![image](https://github.com/dilocho/Pi-Hole-Adblocker/assets/38048735/0ab46b86-4bb7-46be-a2bb-6e2351210e2d)
*Ref 3. Pi Hole Ad Blocker Dashboard*

4. Ads seem to be blocking form some devices but not all. Since still getting a score of 38/100 on ad tester. Seems like 2 devices are in use of the ad blocking one being a wireless extender and another being a mobile device.

![image](https://github.com/dilocho/Pi-Hole-Adblocker/assets/38048735/924085aa-9ba6-40a9-8d21-2467173ff927)
*Ref 4. Pi Hole Device list connected and enabled on*

5. When testing via mobile connected wirelessly to router in a new private browser, ads rate of ads as per test site show that we score a 30 out of 100.

![image](https://github.com/dilocho/Pi-Hole-Adblocker/assets/38048735/3b4ba9f2-1b8d-43aa-befd-0bbca04c9695)
*Ref 5. Ad Blocker Test on device before Pi Hole Enabled*

6. Testing again in a new private browser increased the score to 74 out of 100. 

![image](https://github.com/dilocho/Pi-Hole-Adblocker/assets/38048735/6947d25f-7716-4f5e-bca5-b5030e872cbf)
*Ref 6. Ad Blocker Test on device after Pi Hole Enabled* 




### Skills Learned

- Setting up Pi-hole allowed me to interact with my DHCP configuration and see practically how its use is within the router
- Utilizing hardware appropriate to the application, unfortunately my Raspberry Pi was overloaded and couldn't handle the traffic going through it and had to be shut off 

## References
1. https://www.raspberrypi.com/tutorials/running-pi-hole-on-a-raspberry-pi/
