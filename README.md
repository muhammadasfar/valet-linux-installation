# Valet Linux Installation Guide
Follow the below commands for valet linux installation

## Install PHP
> sudo add-apt-repository ppa:ondrej/php 

> sudo apt-get install software-properties-common 

> sudo apt-get update 

> sudo apt-get -y install unzip zip nginx php7.2 php7.2-mysql php7.2-fpm php7.2-mbstring php7.2-xml php7.2-curl php*-json php*-cli php*-common php*-mcrypt php*-xml php*-zip

## Install LibNSS3Tools
> sudo apt-get install libnss3-tools jq xsel

## Install Composer
> sudo apt-get install composer

## Downgrade version PHP 7.2 / if PHP Version is greater than 7.2
> sudo update-alternatives --set php /usr/bin/php7.2

## Install Package Valet with composer
> composer global require cpriego/valet-linux

**Before the next step please check first in the .config folder whether the vendor is in the composer folder or not, if not yet please cut the vendor folder to .config / composer**

## Install DNSMasq
> sudo apt-get install dnsmasq

## Start WebServer Nginx
> sudo service nginx start

## Check Status WebServer Nginx
> sudo service nginx status

**check if nginx is running, then if it's already running please exit with below command**
> sudo service nginx stop

## Export the PATH so we can install the valet
> echo "export PATH=$PATH:$HOME/.config/composer/vendor/bin" >> ~/.bashrcsource ~/.bashrc

## Install Valet
> valet install

## Create a new directory 
> mkdir ~/Sites

## Change directory
> cd ~/Sites

## Run below command
> valet park

**This command will register your current working directory as a path that Valet should search for sites**

**Add/Create Project in this  ~/Sites directory**

**Access your project using its folder name for example http://directory-name.test**

## Important Valet Commands
###### For https
> Valet secure folder-name
###### For http
> Valet unsecure folder-name
###### Lists existed domains
> Valet domain           
###### Create a domain name and by default its .test
> Valet domain .domainName









