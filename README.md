# Yii 2022-06-14) v0.3
***********************************************



###


## First of all you need to create a new user i use pool, and upgrade the system.

stratum here cd /home/yiimp-data/yiimp/site/stratum/config

screen bash run.sh sha

Update and upgrade your system.
```
sudo apt-get update && sudo apt-get upgrade -y
```
To create your new user and.
```
adduser pool
```
To add you new user to sudo group
```
adduser pool sudo
```
###

### Clone the git repo
- > Be sure you are have su in to your pool user before you clone it, else you clone it to root user

```
sudo su pool
```
### clone the git repo.
```
git clone https://github.com/afiniel/yiimp_install_script.git
```
### cd to the installer map.
```
cd yiimp_install_script
```
### Now it's time to start the installation.
```
bash install.sh
```
- > It will take some time for the installation to be finnished and it will do for you.

***********************************

## This script has an interactive beginning and will ask for the following information :

- Server Name (You can enter )(Example)): example.com or your ip of your vps like this 80.41.52.63)
- Are you using a subdomain (subdomain.example.com)
- Enter support email
- Set stratum to AutoExchange
- Your Public IP for admin access (Put your PERSONNAL IP, NOT IP of your VPS)
- Install Fail2ban
- Install UFW and configure ports
- Install LetsEncrypt SSL

***********************************

Finish! Remember to 
```
sudo reboot
```
when the installer tell you to.

- Access your new pool at (No-SSL) example.com/site/      (With SSL) https://www.example.com/site/
- Access AdminPanel: (No-SSL) example.com/site/AdminPanel (With SSL) https://www.example.com/site/AdminPanel


### Update keys.php if you have exchange (Enable)

- > Update your public keys for exchanges (If Enable). update with Your own keys.. , you can change it by nano to,
```
sudo nano /etc/yiimp/keys.php
```
### Change AdminRights

- > **If you want change your AdminRights to something else :** Edit this file "/SiteController.php" and Line 11 => change 'AdminPanel'

```
sudo nano /var/web/yaamp/modules/site/SiteController.php
```
###### :bangbang: **IMPORTANT** : 

- The configuration of yiimp and coin require a minimum of knowledge in linux
- Your mysql information (login/Password) is saved in **~/.my.cnf**

*****************************************************************************

