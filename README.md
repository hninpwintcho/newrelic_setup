# newrelic_setup
https://github.com/devktops/laravel-todo

Step 1 : First build new APP Server(Ubuntu24) @AWS
ngixn and redis and mariadb set up 

sudo apt update

sudo apt install software-properties-common

sudo apt install nginx redis mariadb-server mariadb-client -y

sudo systemctl status nginx 

sudo systemctl status mysql

sudo systemctl status redis

Step 2 : php install on Ubuntu
sudo apt install -y nginx php8.3 php8.3-fpm php8.3-mysql php8.3-xml php8.3-mbstring php8.3-gd php8.3-curl php8.3-zip php8.3-imagick php8.3-redis php8.3-bcmath php8.3-exif php8.3-ctype php8.3-fileinfo php8.3-tokenizer php8.3-xml

sudo systemctl status php8.3-fpm

sudo apt install git -y

Step 3: check  files
cd /var/www/html
ubuntu@ip-172-26-4-95:/var/www/html$ sudo usermod -aG www-data ubuntu
groups
ubuntu@ip-172-26-4-95:/var/www/html$ sudo chown -R ubuntu:www-data .
ubuntu@ip-172-26-4-95:/var/www/html$ ll
total 12
drwxr-xr-x 2 ubuntu www-data 4096 Feb  6 15:24 ./
drwxr-xr-x 3 root   root     4096 Feb  6 15:24 ../
-rw-r--r-- 1 ubuntu www-data  615 Feb  6 15:24 index.nginx-debian.html

cd /var/www/html/
git clone https://github.com/hninpwintcho/laravel-todo-new.git

Step 4:composer install

curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer

php dependecies installation :
cd laravel-todo-new
composer i

Step 5: nodejs install
cd /var/www/html
sudo apt install nodejs 
node -v

sudo apt install npm
git pull
npm i






