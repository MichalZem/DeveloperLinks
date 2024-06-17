raspi-config Open Raspberry Pi configuration

# Manage software
sudo apt update Check for updates over the Internet  
sudo apt full-upgrade Apply updates to all installed software  
apt search trash Search for an application containing the word trash  
sudo apt install trash-cli Install the trash-cli command  
sudo apt remove foo Uninstall the foo command  
sudo apt purge foo Uninstall the foo command and erase its configuration files  

# Basic Linux commands
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



