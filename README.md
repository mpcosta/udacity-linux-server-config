# Linux Server Configuration

Linux Server Configuration to allow hosting of web applications

## Accessing Details

- IP Address: 35.176.172.7
- SSH Port: 2200

## URL of Application

- http://35.176.172.7

## Summary of Software Installed

- Python 3
- Flask
- PostgreSQL
- Pip 3

- Apache2
- mod_wsgi
- Git

## Configuration Changes Made

- Set up new Ubuntu Linux Server instance on Amazon Lightsail;
- Updated and Upgrade all packages;
- Changed default SSH port 22 to 2200 on the sshd_config file while adding the rule on Amazon Lightsail;
- Set up local environment with Putty in order to gain access to the server by SSH port 2200;
- Configured UFW to only allow incoming connections from SSH (Port 2200), HTTP (Port 80) and NTP (Port 123);
- Checked UFW Status (OK);
- Created a new user called grader with password grader;
- Granted grader sudo permission by adding his file to ~/sudoers.d/;
- Generated SSH Key Pair locally using ssh-keygen and implemented on the server after; 
- UTC Timezone was already set;
- Project built with Python 3 so installed libapache2-mod-wsgi-py3
- Installed Apache2 and PostgreSQL
- Configured PostgreSQL to not allow remote connections by checking its conf file;
- Created new user named catalog and db named catalog;
- Granted permissions from user named catalog to catalog application database;
- Installed Git;
- Cloned the Catalog Project https://github.com/mpcosta/Item-Catalog-Web-Application.git;
- Changed paths from sqllite to allow PostgreSQL;
- Set up server correctly by configuring apache2 flask app .wsgi files with correct parameters;
- Moved project from current directory to /var/www/FlaskApp;
- a2ensite flask.conf file
- Restarted Apache2 Service
- Loaded URL (OK); 