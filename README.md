# windows-ubuntu-subsystem
- sudo apt-get install apache2
- sudo service apache2 start
- sudo apt-get install mysql-server
- sudo service mysql start

- sudo -i
- mysql
- mysql> exit;
- mysql> CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password';
- mysql> GRANT ALL PRIVILEGES ON * . * TO 'newuser'@'localhost';

- sudo apt-get update
- sudo apt-get install php libapache2-mod-php php-mysql

- cd /var/www/html
- create test.php file <?php phpinfo(); ?>

## Silverstripe Dependencies
- sudo apt-get install php-gd
- sudo apt-get install php-xml
- sudo apt-get install php-intl
- sudo apt-get install php-curl
- sudo apt-get install php-tidy
- sudo apt-get install php-mbstring

# Enable mod_rewrite
- sudo a2enmod rewrite
- Add this to 'sudo nano /etc/apache2/sites-available/000-default.conf' before '</VirtualHost>'
`<Directory /var/www/html>
        Options Indexes FollowSymLinks MultiViews
        AllowOverride All
        Require all granted
</Directory>`

# Update php.ini
- date.timezone = "US/Central"
- extension=php_curl
- extension=php_gd2
- extension=php_intl

# Install composer
sudo apt-get update
sudo apt-get install curl
sudo curl -s https://getcomposer.org/installer | php
sudo mv composer.phar /usr/local/bin/composer

# Install silverstripe-elemental from https://github.com/dnadesign/silverstripe-elemental




