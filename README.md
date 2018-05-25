# php7-apache-dev
PHP 7.1|7.2 FPM from webdevops:php-apache-dev

PHP 7.1 FPM + Apache + Ubuntu 16.04
================

## docker-compose.yml

```docker-compose
version: "2"
services:
  php:
    image: saraivagilberto/php7.1-apache-dev
    ports:
      - "80:80"    
    volumes:
      - ./html:/var/www/html
    environment:
      WEB_DOCUMENT_ROOT: "/var/www/html"
      WEB_PHP_TIMEOUT: 600
      PHP_DEBUGGER: "xdebug"
      XDEBUG_REMOTE_AUTOSTART: 1
      XDEBUG_REMOTE_CONNECT_BACK: 0
      XDEBUG_REMOTE_HOST: 192.168.0.1
      XDEBUG_REMOTE_PORT: 9001      
```

## php-fpm -v

```
PHP 7.1.17-1+ubuntu16.04.1+deb.sury.org+1 (fpm-fcgi) (built: May  5 2018 04:55:21)
Copyright (c) 1997-2018 The PHP Group
Zend Engine v3.1.0, Copyright (c) 1998-2018 Zend Technologies
    with Zend OPcache v7.1.17-1+ubuntu16.04.1+deb.sury.org+1, Copyright (c) 1999-2018, by Zend Technologies
    with Xdebug v2.6.0, Copyright (c) 2002-2018, by Derick Rethans
```

PHP 7.2 FPM + Apache + Ubuntu 16.04
================

## docker-compose.yml

```docker-compose
version: "2"
services:
  php:
    image: saraivagilberto/php7.2-apache-dev
    ports:
      - "80:80"    
    volumes:
      - ./html:/var/www/html
    environment:
      WEB_DOCUMENT_ROOT: "/var/www/html"
      WEB_PHP_TIMEOUT: 600
      PHP_DEBUGGER: "xdebug"
      XDEBUG_REMOTE_AUTOSTART: 1
      XDEBUG_REMOTE_CONNECT_BACK: 0
      XDEBUG_REMOTE_HOST: 192.168.0.1
      XDEBUG_REMOTE_PORT: 9001      
```

## php-fpm -v

```
PHP 7.2.5-1+ubuntu16.04.1+deb.sury.org+1 (fpm-fcgi) (built: May  5 2018 04:59:13)
Copyright (c) 1997-2018 The PHP Group
Zend Engine v3.2.0, Copyright (c) 1998-2018 Zend Technologies
    with Zend OPcache v7.2.5-1+ubuntu16.04.1+deb.sury.org+1, Copyright (c) 1999-2018, by Zend Technologies
    with Xdebug v2.6.0, Copyright (c) 2002-2018, by Derick Rethans
```
