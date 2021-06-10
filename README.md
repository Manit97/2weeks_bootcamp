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

-sudo apt-get update -y 
-sudo apt-get upgrade-y
-sudo apt-get install nginx
-sudo systemctl restart nginx
-sudo apt-get install nodejs -y 
-sudo apt-get install python-software-properties 
-curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
-sudo apt-get install nodejs -y
-sudo npm install pm2 -g
-npm install