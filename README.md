# FSND-Linux-Server-Configuration

This is a instruction for the grader for the Linux Server Configuration asssigment from the Udacity Full Stack Nano Degree.

## The IP address and SSH port

The server can be accessed through SSH on port 2200 of [ec2-52-57-232-101.eu-central-1.compute.amazonaws.com](ec2-52-57-232-101.eu-central-1.compute.amazonaws.com)

```
ssh -i ssh-key grader@ec2-52-57-232-101.eu-central-1.compute.amazonaws.com -p 2200
```
(The server is accessed using the SSH key as submitted in the instructor notes, so not accessible by the public)

## URL of the hosted web application

The application can be visited on http://ec2-52-57-232-101.eu-central-1.compute.amazonaws.com


## Summary of software installed and configuration changes made

Software installed through apt-get:
- apache2
- libapache2-mod-wsgi
- postgresql 
- postgresql-contrib
- git
- python
- python-pip

Software installed through pip:
- flask 
- sqalchemy
- oauth2client
- virtualenv

Configuration changes made
- Linux system users added 
- Sudo permisions given for grader
- SSH authentication setup for grader
- Changed UFW (Uncomplicated Firewall) according to assignment requirements
- psql users added
- psql database created

Catalog app files added to /var/www/ using git

Files modified
- /etc/apache2/sites-enabled/000-default.conf to point to custom .wsgi file 
- main app file to correct paths and change db to use psql
- db_setup file to populate psql db instead of sqlite db)

## Third-party resources used
- https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-14-04
- https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
- www.stackoverflow.com
- Udacity discussions forum
- https://github.com/skh/fsnd-linux-server-config (reference from Udacity discussions)
