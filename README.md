# rpi-opencv-playbook


This is an Ansible playbook that will install opencv and all it's dependencies on the raspbian

# How to use

 You will need a linux box with ansible installed and operational.

 Flash SD card and install rasbian as usual except skipping the package upgrade step.  Ensure the
 camera and ssh are enable (raspi-config) and reboot.
 
 Ensure you can SSH into your rpi from a linux box. Disconnect.  From you linux box issue this command:
 
## ssh-copy-id pi@192.168.xxx.xxx (address to you rpi)
 
 Now SSH back into your rpi.  You should be signed into your rpi without having to give your password. 
 
 Disconnect from rpi
 
 On your linux box edit /etc/ansible/hosts and add
 
 ## [picam1]
 ## 192.168.xxx.xxx (address to your rpi)
 
 Then clone this repo and run the playbook
 
 git clone https://github.com/cjsmocjsmo/rpi-opencv-playbook.git
 
## cd ./rpi-opencv-playbook && ansible-playbook rpi-opencv-install.yml

# NOTE

I have not used a virtualenviroment on purpose.  This setup may not survive a system upgrade so use with caution.
 
 
 
 
 
 
 
 
 

