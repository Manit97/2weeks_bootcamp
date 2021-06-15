# 2weeks_bootcamp

## Introduction to Devops
- Breaking down silos and bringing developers and operations closer together
- Share responsibilities
- Deploy infrastructure as code
- Automate the deployment pipleine as much as possible
- Supported by strong CI/CD pratices

## Linux commands that work on Bash
### Folder and Terminal
- Create a Dir 'mkdir name_of_file'
- Go Inside Dir 'cd name_of_dir'
- Come out of Dir 'cd ..'
- Who I am 'uname -a'
- Where I am 'pwd'
- Create a file 'touch name_of_file' or 'nano File_name' you land inside the file
- Exit from nana 'ctrl x' then enter
- List everything 'ls -a' or 'ls'
- To see the content of the file on the terminal 'cat file_name'
- Clear your screen 'clear'

- Delete a folder 'rm -rf name_of_the_folder'
- Delete a file 'rm name_of_the_file'

### Linux Systems/Programs
- 'sudo apt-get update -y' in VM to update Linux
- 'sudo apt-get upgrade-y' in VM to upgrade Linux
- 'sudo apt-get install nginx' in VM to install NGINX (web server)
- 'sudo systemctl enable nginx' in VM to enable nginx
- 'sudo systemctl stop nginx' in VM to stop nginx
- 'sudo systemctl status nginx' in VM to check server status
- 'sudo systemctl restart nginx' in VM to restart server
- 'sudo apt-get remove nginx' to uninstall nginx
- 'sudo bash provision.sh' to execute this bash file
- 'sudo chmod +x provision.sh' makes the bash file executable and you can now run it by ‘sudo ./provision.sh’
- 'sudo su' to make you root admin
- 'history' to see your previous commands

### Vagrant
- To initialise vagrant 'vagrat init'.
- To start vagrant 'vagrant up'.
- To SSH into vagrant 'vagrant ssh'.
- To suspend the vagrant 'vagrant suspend'.
- To reload vagrant 'vagrant reload'.
- To destroy vagrant 'vagrant destroy'.

### Bash Script
#!/bin/bash

- sudo apt-get update -y 
- sudo apt-get upgrade-y
- sudo apt-get install nginx
- sudo systemctl restart nginx
- sudo apt-get install nodejs -y 
- sudo apt-get install python-software-properties 
- curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
- sudo apt-get install nodejs -y
- sudo npm install pm2 -g
- npm install

### App Instance Vm
- sudo chmod 400 devop_bootcamp.pem (in your .ssh folder)
- ssh -i "devop_bootcamp.pem" ubuntu@ec2-{I-P}.eu-west-1.compute.amazonaws.com (To ssh into the app vm)
- sudo scp -i ~/.ssh/devop_bootcamp.pem -r app/ ubuntu@ec2-54-78-10-214.eu-west-1.compute.amazonaws.com:/home/ubuntu/ (to transfer app folder to app vm from .ssh folder)
- cd /etc/nginx/sites-available (and edit default file for reverse proxy)
-server {
-        listen 80;
-        server_name _;
-        location / {
-                proxy_pass http://54.78.10.214:3000;
-                proxy_http_version 1.1;
-                proxy_set_header Upgrade $http_upgrade;
-                proxy_set_header Connection 'upgrade';
-                proxy_set_header Host $host;
-                proxy_cache_bypass $http_upgrade;
-        }
- } 
- Above Code goes in the default file. 
- In app/seeds and run the seed file with ‘node seed.js’ (To make posts work)


