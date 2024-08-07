# Rasberry PI CheatSheets

# Commom command
sudo raspi-config
journalctl -fu servicename.service


## Other Links
https://gist.github.com/hofmannsven/9132419

## MQTT
https://mntolia.com/10-free-public-private-mqtt-brokers-for-testing-prototyping/  
https://www.hivemq.com/mqtt/public-mqtt-broker/  
https://console.hivemq.cloud/  

#### MQTT Clients
https://mqtt-explorer.com/  
https://mqttx.app/  
https://mqttboard.flespi.io/#/  
https://www.bevywise.com/mqtt-broker/ - Enterprise  

## Shop
## Remote Access
https://connect.raspberrypi.com/  
https://www.raspberrypi.com/documentation/services/connect.html#enable-remote-shell-at-all-times  
  
https://www.dataplicity.com/  
https://www.pitunnel.com/  
https://dashboard.pinggy.io/ - free na 60minut jeden tunel  
https://dashboard.ngrok.com/  
https://docs.zrok.io/docs/guides/install/linux/  
https://app.tunnelin.com/  
https://loophole.cloud/docs  
https://theboroer.github.io/localtunnel-www/  


## Common 
raspi-config Open Raspberry Pi configuration

## Manage software
sudo apt update Check for updates over the Internet  
sudo apt full-upgrade Apply updates to all installed software  
apt search trash Search for an application containing the word trash  
sudo apt install trash-cli Install the trash-cli command  
sudo apt remove foo Uninstall the foo command  
sudo apt purge foo Uninstall the foo command and erase its configuration files  

## Basic Linux commands
ls List contents of current directory  
cd ~ Change directory to your home directory  
cd ~/Documents Change directory to your Documents directory  
cd .. Change directory up one level  
touch ~/Documents/file.txt Create or update modification time of file.txt  
nano ~/Documents/file.txt Open file.txt in the terminal text editor nano (Ctrl+X to exit)  
cat ~/Documents/file.txt Print the contents of file.txt to the terminal  
less ~/Documents/file.txt View the contents of file.txt In the terminal (Q to quit)  
file ~/Documents/file.txt Print what kind of data file.txt contains  
trash ~/Documents/file.txt Place file.txt into the Trash folder  
du -h ~ Print the disk space that's been used  
df -h ~ Print the disk space that's free  
man du View the manual for the du command  
lsblk List block devices (hard drives) connected to your Pi  
date Print the current date  



# Instalace užitečných balíčku
sudo apt install screen - more console and terminal multiplexer
sudo apt install mc - midnight commander
sudo apt install webmin - UI WEB admin portal for Linux


# Teplomer DS18B20
IOT knihovna MS Dotnet -  https://github.com/dotnet/iot/blob/main/src/devices/OneWire/README.md  
https://charlieblog.eu/clanek-raspberry-pi-meteostanice-ds18b20  
Multiple Temp - https://www.hackster.io/vinayyn/multiple-ds18b20-temp-sensors-interfacing-with-raspberry-pi-d8a6b0  

# Camera 
.NET Camera - https://neilsnotes.net/Software/Coding/dotnetPiCam.html   -   https://www.youtube.com/watch?v=haY_wMKHq-E   - https://www.youtube.com/watch?v=-KYH78spofs
https://learn.microsoft.com/en-us/answers/questions/1608328/getting-recording-to-work-with-multiple-usb-camera  

# PWM
https://randomnerdtutorials.com/raspberry-pi-pwm-python/

