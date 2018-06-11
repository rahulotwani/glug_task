1.
cd Desktop 
mkdir audio
cd audio
touch song{1..10}.mp3
cd ..
ln -s  ../Desktop/audio ../Desktop/music


2.
sudo su
groupadd sysadmin
groupadd manager
useradd  bob
useradd  rob
useradd  max
passwd bob
passwd rob
passwd max
usermod -g sysadmin bob
usermod -g sysadmin rob
usermod -g sysadmin max
usermod -g manager bob
usermod -g manager rob


3.
vim /etc/passwd
and edit max:x:1003:1005::/home/max:/bin/bash
to max:x:1003:1005::/home/max:/bin/false
sudo chage bob
//set password expiration warning to 30 days
sudo chage max
//set password inactive in 30 days


4.
mkdir /home/manager
chgrp manager /home/manager
sudo chmod 2770 /home/manager


5.
useradd -u 4223 gabriel
passwd gabriel


6.
mkdir /tmp/var 
tar -cvjf /tmp/var/archive.tar.bz2 /etc/hosts


7.
sudo grep udp /etc/services > udp_services.txt


8.
top then shift+f then s to set the sort then esc to go back to the main screen of top


9.
alias
alias=’yo’
alias yo=”/bin/uptime”


10.
sudo apt-get install vim
vim hello.txt press i for insert mode and esc to go back to command mode In insert mode we can type like regular text editor In command mode x - del :q! - quit without saving :wq - save and quit


11.
do apt-get install firewalld sudo firewall-cmd --get-default-zone sudo firewall-cmd --set-default-zone=dmz sudo firewall-cmd --get-zones > zones.txt


12.
firewall-cmd --zone=public --add-port=8080/tcp --permanent sudo netstat -ntlp | grep LISTEN > zones.txt
​

13.
 sudo iptables -t nat -A PREROUTING -i eth0 -p tcp --dport 80 -j REDIRECT --to-port 8080

