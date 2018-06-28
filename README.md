# How to setup LAMP stack development environment
Install python setuptools, git, pip & virtualenv
```
$ python -V or pythonx -V #Check python version, if found python2.7 go without python2.7 installation step else install python2.7

$ sudo apt-get install python2.7 # Install Python2.7 

$ wget https://bootstrap.pypa.io/get-pip.py && sudo python get-pip.py # Install pip tool

$ sudo apt-get install build-essential libssl-dev libcurl4-gnutls-dev  libexpat1-dev gettext zip unzip # Install essential packages

$ sudo apt-get install git # Install git

$ git --version

# Install virtual env, create virtual env with python2.7 and activate virtual env to be used for django project
$ sudo pip install virtualenv

$ mkdir ENVS && cd ENVS

$ virtualenv -p /usr/bin/python2.7 samm-virt-env # Make sure python executable path is correct

$ source samm-virt-env/bin/activate

```

# Install other necessary libraries

```
$ sudo apt-get build-dep python-imaging

$ sudo apt-get install libjpeg8 libjpeg62-dev libfreetype6 libfreetype6-dev

$ sudo apt-get install libmysqlclient-dev

$ sudo apt-get install python-dev 
```
# Installing django and other essential site-packages

```
$ pip install django==1.8 # Install django 1.8

$ pip install Pillow

$ pip install MySQL-python

$ pip install xlrd
```
# Installing Apache2

```
$ sudo apt-get install apache2

$ sudo apt-get install libapache2-mod-wsgi

$ sudo a2enmod wsgi

$ chmod o+x /home/user && ls -l /home/ # To avoid forbidden access error while running django app from home (non-root) directory with apache2

$ sudo service apache2 restart
```
# Installing MySQL database

```
$ sudo apt-get install mysql-server
``
