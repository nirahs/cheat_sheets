# Server

## Local Server

### Login via SSH with password to local server

`$ ssh [user_name]@[server_ipaddress]`

#### Create folder, file, install Apache

`$ mkdir [folder_name]`

`$ cd [folder_name]`

`$ touch [folder_name]`

`$ sudo apt-get install apache2`

> Apache is the most well known web server. Web server is the tool which handles the https requests and return the files according to the get request. NGINX is safer than apache.

#### Generate Keys

`$ ssh-keygen`

#### Add public key to server in one command

`> cat ~/.ssh/id_rsa.pub | ssh [username]@[server_ipaddress] "mkdir -p ~/.ssh && chmod 700 ~/.ssh && cat >>  ~/.ssh/authorized_keys`

#### Create & copy a file to the server using SCP

`$ touch test.txt`

`$ scp ~/test.txt [username]@[server_ipaddress]:~`

## Remote Server

### Create Keys for remote server

`$ ssh-keygen -t rsa 4096`

> Create account in the remote server and add public key when creating the account.

> Here `rsa` is an algorithm which is used to generate ssh keys. And `4096` means key will contain 4096 characters so it will unique and secure.

### Add the ssh key to ssh-agent

`$ ssh-add ~/.ssh/id_rsa_do`

### Logging in

`$ ssh root@[server_ipaddress]`

### Update packages (ubuntu)

> Package managers are different for each linux distribution.

`$ sudo apt update`

`$ sudo apt upgrade`

### Create new user with sudo

`$ adduser [username]`

`$ id [username]`

`$ usermod -aG sudo [username]`

`$ id [username]`

### Login as newly created user

`$ ssh [username]@[server_ipaddress]`

### Adding the ssh keys to newly created user .ssh folder

> On the server, log back in as root because only root can access the .ssh folder.

`$ ssh root@[server_ipaddress]`

> Folder structure change for different distibution or OS. So do a research.

`$ cd /home/[username]`

`$ mkdir .ssh`

`$ cd .ssh`

`$ touch [authorized_keys]`

`$ sudo nano [authorized_keys]`

> Paste in the id_rsa_do.pub key, save, exit and log in as newly created user

### Disable root password login

> To prevent the remote server from bruteforce attack.

`$ sudo nano /etc/ssh/sshd_config`

#### Set the following

`PermitRootLogin no`

`PasswordAuthentication no`

## Reload sshd service

`$ sudo systemctl reload sshd`

## Change owner of /home/[username]/* to [username]

> For read and write privalages for all the files and folder.

`$ sudo chown -R [username]:[username] /home/[username]`

## Setting permission

`$ chmod 700 /home/[username]/.ssh`

## Install Apache (web server) and visit ip

> Web server is used to visit the ipaddress using browser. Web server can manage the http request and return content back.

`$ sudo apt install apache2 -y`

## Generate Github Key (On Server)

> [Setting SSH for github account](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

> [Testing SSH connection for github account](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/testing-your-ssh-connection)

> [Reviewing SSH keys in github account](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/reviewing-your-ssh-keys)

`$ ssh-keygen -t rsa`

## Add new key

`$ ssh-add /home/[username]/.ssh/id_rsa_github`

## If you get a message about auth agent, run this and try again

`$ eval 'ssh-agent -s'`

## Clone repo

`$ git clone git@github.com:[account_name]/[public_repo].git`

## Install Node JS to compile javascript

`$ curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -`

`$ sudo apt-get install -y nodejs`

## Install Dependencies

`$ npm install`

## Start Dev Server and visit ip:3000

`$ npm start`

## Build Out React App

`$ npm run build`

## Move static build to web server root

`$ sudo mv -v /home/[username]/[project_folder_name]/build/* /var/www/html`
