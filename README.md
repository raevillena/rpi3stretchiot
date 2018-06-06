# rpi3stretchiot
How to setup Raspberry pi 3 with Raspbian stretch

with Apache2, mysql/mariadb, php7.0, phpmyadmin, node-red

sudo apt-get update #update repo 

sudo apt-get upgrade -y #install new repo versions

sudo apt-get install mariadb-server mariadb-client -y #install sql database

sudo apt-get install apache2 php7.0 libapache2-mod-7.0 php7.0-mysql phpmyadmin -y  

sudo mysql_secure_installation #set mariadb root password 

sudo service mysql reload sudo mysql -u root -p #check if password is working 

sudo service apache2 reload

update-nodejs-and-nodered #update the built-in node-red to have it properly working

sudo systemctl enable nodered.service  

MariaDB [(none)]> USE mysql;

MariaDB [(none)]> UPDATE user SET password=PASSWORD('YourPasswordHere') WHERE User='root' AND Host = 'localhost';

MariaDB [(none)]> FLUSH PRIVILEGES; 

GRANT ALL PRIVILEGES ON *.* TO 'root'@'localhost' IDENTIFIED BY 'nodeberic';

FLUSH PRIVILEGES;
