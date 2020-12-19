# rpi-opencv-playbook


This is an Ansible playbook that will install opencv and all it's dependencies on raspbian (raspberry pi OS).  You can setup 1 or 100 all at the same time just edit /etc/ansible/hosts accordingly. 

# How to use

 You will need a linux box with ansible installed and operational.

 Flash SD card and install rasbian as usual except skipping the package upgrade step.  Ensure the camera and ssh are enabled (raspi-config) and reboot.
 
 Ensure you can SSH into your rpi from a linux box. Disconnect.  From your linux box issue this command:
 
## ssh-copy-id pi@192.168.xxx.xxx (address to your rpi)
 
 Now SSH back into your rpi.  You should be signed into your rpi without having to give your password. 
 
 Disconnect from rpi
 
 On your linux box edit /etc/ansible/hosts and add
 
 ## [picam1]
 ## 192.168.xxx.xxx (address to your rpi)
 
 Then clone this repo and run the playbook
 
 git clone https://github.com/cjsmocjsmo/rpi-opencv-playbook.git
 
## cd ./rpi-opencv-playbook
## ansible-playbook rpi-opencv-install.yml

# NOTE

I have not used a virtual environment on purpose.  I am an advocate of using a virtual environment when developing a python program but I would argue that a virtual environment in a production setting is not needed.

When you apt-get install python3-yaml does it setup a virtual environment and place python3-yaml in it?  No it does not.

When you pip3 install python3-yaml does it setup a virtual environment and place python3-yaml in it?  No it does not.

So why add an extra layer of code that brings little to no value in a production environment. (I like my rpi's lean and mean)

Due to the use of pip this setup may not survive a system upgrade so use with caution.
 
 
 
 
 
 
 
 
 

