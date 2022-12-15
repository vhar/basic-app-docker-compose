# Basic PHP Web Application Docker Template #
It's my favorite template for quick start design new web project  
This template contains **nginx**, **php8.1-fpm**, **mariadb** and **composer** containers  
**php-fpm** contains the following extensions:  
```
bz2
calendar
common
ctype
curl
dom
fileinfo
ftp
gd
gettext
iconv
interbase
intl
mbstring
mysqli
mysqlnd
opcache
pdo
phar
posix
simplexml
soap
sockets
tokenizer
xdebug
xml
xmlreader
xmlrpc
xmlwriter
xsl
zip
```
If you need to add other extensions, make the necessary changes to the **./provisioning/docker/php/Dockerfile** file

### How to use ###
1. Clone a repository
2. Create **.env** file
3. Define APP_NAME and MARIADB_ROOT_PASSWORD environment variables  
for example:
```
APP_NAME=example.com
MARIADB_ROOT_PASSWORD=secret
```
4. Create a folder with the same name as the APP_NAME environment variable and put your website code in it
5. Run docker-compose

You project is available at http://localhost or http://{APP_NAME}  
phpMyAdmin is available at http://localhost:8081 

### composer usage ###
Run from console at repository root folder (that contains docker-compose.yml file) **docker-compose run --rm composer <composer command>**  
for example:  
```
docker-compose run --rm composer require vhar/sberbank
```

### error log files ###
You can find error logs in ./.docker folder  
Change permission to 0777 for ./.docker/php folder
