# Linux Server Configuration
***
### Introduction
This project is about configuring Linux server for live running web application. This Linux server has been configured using on lightsail amazon server with AWS.

### Features
* Server is running ItemCatalog Web application which uses PostgreSQL database sever  
* Firewall for server has been configured which allows connection only for SSH(port 2200), HTTP (port 80), and NTP (port 123).  
* Key-based authentication is enforced and password authentication is disabled  

### Software installed on the server:
pip, virtualenv, PostgreSQL datababse server, Apache2, WSGI

### Library for Web application
Flask, SQLalchemy, oauth2clien, httplib2, requests

### IP address for the server
52.91.97.5

## Configuration Steps:

1. Updated and upgraded default system packages using 
    `sudo apt-get update` and `sudo apt-get upgrade`
2. Configure firewall using `ufw` package
3. Open port for `ssh(22), HTTP(80) and NTP(123)`
4. changed ssh port from the default 22 to 2200
5. Created second user with name "grader"
6. Changed User accessibility for grader user and added "grader" in sudoers
7. Enable key-based authentication for "grader" and default user "ubuntu" using system package `ssh-keygen`
8. Disable Password authentication for "grader" (Lighsail Amazon (AWS) linux server usually has password authentication off for default use)
9. Install APache2 and WSGI to run web application on the server
10. Clone the Project(Web Application) repo from the github
11. Made changes in WSGI configuration and Tested the application

### Frequent Linux command
- ls, rm (also with recursive flag -R), cd, pwd, man, mkdir, mv, cp 
- touch, nano/vi, cat
- chmod, chown
- /etc/init.d/apache2 restart [also start and stop ] (can be used for any other init process)
- sudo apache2ctl restart, ifconfig
- apt-get install
- apt-get puge/ apt-get remove

### NOTE
Locally, practiced all the step using vagrant with virtualbox. All the Vagrant files are include in this repo.
- Steps to use vagrant are mentioned in the project "https://github.com/bittu072/Tournament"
- Repo for ItemCatalog-sport web aplication : "https://github.com/bittu072/ItemCatalog-Sport"

### Reference
- https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
- Udacity Forums
