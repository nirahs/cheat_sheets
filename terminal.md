# Terminal Commands

## Commands

## Print working directory

`$ pwd`

## Change directory

`$ cd`

## Change to folder directory

`$ cd [folder_name]`

## Change to previous/higher directory

`$ cd ..`

## List directory and files

`$ ls`

## List all directory and files including hidden items

`$ ls -a`

## List directory and files with permission

`$ ls -l`

## Clear the terminal

`$ clear`

## Create directory called folder in current directory

`$ mkdir folder`

## Create directory with space in thier name

`$ mkdir [folder_name_1]\ [folder_name_2]`

`$ mkdir "[folder_name_1] [folder_name_2]"`

## Remove folder from current directory (Permanently)

`$ rmdir [folder_name]`

## Remove direc1 and direc2 from current directory (Permanently)

`$ rmdir [folder_name] [folder_name]`

## Creates index.html file

`$ touch index.html`

## Creates index.html and style.css files

`$ touch index.html style.css`

## Remove file called index.html from current directory (Permanently)

`$ rm index.html`

## Remove index.html and style.css from current directory (Permanently)

`$ rm index.html style.css`

## Remove all the files with the folder. (-r: Recursive)

`$ rm -r [folder_name]`

## Remove all the files with the folder without propmting. 

`$ rm -rf [folder_name]`

## To access the manual of a flags for each command (man rm, man rmdir)

`$ man ls`

## Copy a file from test folder and pasting in Desktop folder. (./ - current directory)

`$ cp test/index.html Desktop`

## Copy test folder from home folder and pasting in Desktop folder

`$ cp -r test Desktop`

## Move test folder from desktop folder to test folder

`$ mv Desktop/test ./test`

## Renaming the files

`$ mv index.html index2.html`

## Print location of the folder

`$ which direc2`

## Generating a locate database

`$ sudo launchctl load -w /System/Library/LaunchDaemons/com.apple.locate.plist`

## Locating files

`$ locate index.html`

## Updating database

`$ updatedb`

## Show last 500 commands

`$ history`

## Changing the password from terminal

`$ passwd`

## Show the network connections

`$ ipconfig`

## Pinging a website. Check whether a website is up or not

`$ ping google.com`

## System monitor

`$ top`

## Disk partitions

`$ df`

## Getting installed application hash

> Hashing algorithm will be mention in the website with hash code to compare.

`openssl [hashing_algorithm] [installed_app.extension]`
