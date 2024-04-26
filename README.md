# commands for ubuntu 22

sudo apt install nginx php-fpm -y

sudo apt install mysql-server -y

sudo apt install net-tools

sudo mysql

ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

quit



sudo apt install phpmyadmin



sudo ln -s /usr/share/phpmyadmin /var/www/html
sudo nano /etc/nginx/sites-enabled/default







server {

       listen 80 default_server;

       listen [::]:80 default_server;

       
        
        root /var/www/html;



       index index.html index.php



       server_name _;

       
        location / {

        try_files $uri $uri $uri/ =404;

      }



       location ~ \.php$ {

                 include snippets/fastcgi-php.conf;

                 fastcgi_pass unix:/run/php/php8.1-fpm.sock;

                 }

                 }
