# born2beroot

This project aims to introduce you to the wonderful world of virtualization.


# Tutorial

https://github.com/gemartin99/Born2beroot-Tutorial/blob/main/README_EN.md

# The Commands Using in Evaluation
## Simple setup
1. Check UFW service
   
   sudo ufw status     or    sudo service ufw status
2. Check SSH service
   
   sudo service ssh status
3. Check the operating system
   
   uname -v

## User
1. checking the group users

      getent group <groupname> 
   
2. creating a new user

      sudo adduser <username>                 

3. creating  a new group

      sudo addgroup <groupname>               

4. assign a group to a user

      sudo adduser <username> <groupname>      

## Hostname and partitions
sudo hostnamectl set-hostname <newname>   # rename the hostname

sudo reboot                               # reboot the VM

lsblk                                     # list the partitions

## SUDO
dpkg -s sudo                              # checking if the sudo is installed

cd /var/log/sudo                          # go to sudo folder

cat sudo_config                           # checking the content of sudo_config

sudo cat sudo_config                      # execute a sudo command and checking if the sudo_config log is updated or not

## UFW
sudo ufw status  /  sudo ufw status numbered     # list all the existent rules

sudo ufw allow 8080                       # adding a new rule 8080

sudo ufw delete allow 8080                # delete the rule 8080

sudo ufw delete <ID>                      # you also can delete a rule using the ID that in the list that you get using 'sudo ufw status numbered'

## SSH
sudo service ssh status                   # checking the ssh status

### login through ssh in another terminal
ssh <username>@localhost -p 4242          # localhost can change to IP address, 4242 is the allowed port to establish the connection

## Script monitoring
sudo crontab -u root -e                   # modify the cron

sudo systemctl stop cron                  # stop the cron

sudo systemctl start cron                 # start the cron

# My Results of Born2beroot
<img width="837" alt="Screen Shot 2024-05-28 at 7 53 21 AM" src="https://github.com/Sherry5Wu/born2beroot/assets/132613292/2d6a2f05-ad62-4c26-b89c-d8dc235c65ac">
