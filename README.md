### Create working directories on your server
```shell script
$ mkdir /home/wordpress /home/wordpress/mysql /home/wordpress/wp-content
```
### Go to WP directory on your server
```shell script
cd /home/wordpress
```
### Upload and install wp-cli:
```shell script
$ curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
$ chmod +x wp-cli.phar
$ mv wp-cli.phar wp
```

### Run docker-compose
```shell script
$ docker-compose up -d
```
#### Open WP http://localhost/wp-admin in browser and install CMS and create user admin

### Next go to container console

$ docker exec -it wordpress_wordpress_1 bash

### Install and activate plugin "Google Authenticator"
```shell script
$ wp plugin install miniorange-2-factor-authentication --allow-root
$ wp plugin activate miniorange-2-factor-authentication --allow-root
```
### Install in your mobile phone application "Google Authenticator" and open it

#### After enteringing of your login and password, please select in the list "Google / Authy / Microsoft Authenticator (Any TOTP Based Authenticatior App)"
#### Scan the QR code and enter the verification code.
