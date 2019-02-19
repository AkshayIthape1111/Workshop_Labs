# How to Setup The Wordpress On Local System 

### Step 1 - System Update And Upgrade
```
sudo -s
apt update
apt upgrade
```
### Step 2 - Apache2 Server Installation
```
apt install apache2
```
### Step 3 - PHP Installation
```
apt install php7.1 libapache2-mod-php7.1 php7.1-common php7.1-mbstring php7.1-xmlrpc php7.1-soap php7.1-gd php7.1-xml php7.1-intl php7.1-mysql php7.1-cli php7.1-mcrypt php7.1-zip php7.1-curl
apt-add-repository ppa:ondrej/php
apt update
apt install php7.1 libapache2-mod-php7.1 php7.1-common php7.1-mbstring php7.1-xmlrpc php7.1-soap php7.1-gd php7.1-xml php7.1-intl php7.1-mysql php7.1-cli php7.1-mcrypt php7.1-zip php7.1-curl
```
### Step 4 - Mysql Database Server Installation
```
apt-get install software-properties-common
apt-key adv --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 0xF1656F24C74CD1D8
add-apt-repository 'deb [arch=amd64,arm64,i386,ppc64el] http://mirror.nodesdirect.com/mariadb/repo/10.3/ubuntu xenial main'
apt-get update
apt install mariadb-server
```
### Step 5 - Setup Directory For Wordpress Project
```
mkdir /var/www/html/workshop1.linuxgeek.in/
wget https://wordpress.org/latest.tar.gz
tar -xzvf latest.tar.gz
cp wordpress/. /var/www/html/workshop1.linuxgeek.in/ -R
cp /var/www/html/workshop1.linuxgeek.in/wp-config-sample.php /var/www/html/workshop1.linuxgeek.in/wp-config.php
chown ubuntu:www-data /var/www/html/workshop1.linuxgeek.in/
```
### Step 6 - Create The Database In Mysql For Our Project
```
mysql -uroot -p
create database wordpress;
exit
```
### Step 8 - Configure The Wp-config File 
```
cd /var/www/html/workshop1.linuxgeek.in/
vi wp-config.php
    database='wordpress'
    username='root'
    password='devops'
```
### Step 9 - Write The Virtual Host File 
```
vi /etc/apache2/sites-available/workshop1.linuxgeek.in.conf

<VirtualHost *:80>
    ServerAdmin webmaster@localhost
    ServerName workshop1.linuxgeek.in
    DocumentRoot /var/www/html/workshop1.linuxgeek.in
   <Directory /var/www/html/workshop1.linuxgeek.in>
        Options Indexes FollowSymLinks MultiViews
        AllowOverride All
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/wordpress-error.log
    CustomLog ${APACHE_LOG_DIR}/wordpress-access.log combined

</VirtualHost>

:wq

a2ensite workshop1.linuxgeek.in.conf
systemctl restart apache2
```
### Step 10 - Add The Entry In /etc/hosts file 
```
vi /etc/hosts

add following line 

127.0.0.1	workshop1.linuxgeek.in

:wq
```
### Step 11 - Open The Browser And Type Your URL 
```
http://workshop1.linuxgeek.in
```
### Step 12 - Setup Wordpress 
### Step 13 - Congratulations You Done It
### Step 14 - Domain Pointing
### Step 15 - SSL Certification Installation 
```
sudo add-apt-repository universe
sudo add-apt-repository ppa:certbot/certbot
sudo apt-get update
sudo apt-get install certbot python-certbot-apache 
```
### Step 16 - Genrate The Certification For Our Domain
```
sudo certbot --apache
```

### Step 17 - Change the Apache Setting 
```
<VirtualHost *:80>
    ServerAdmin webmaster@localhost
    ServerName workshop1.linuxgeek.in
    DocumentRoot /var/www/html/workshop1.linuxgeek.in
    Redirect / https://workshop1.linuxgeek.in
    ErrorLog ${APACHE_LOG_DIR}/wordpress-error.log
    CustomLog ${APACHE_LOG_DIR}/wordpress-access.log combined

</VirtualHost>
```
