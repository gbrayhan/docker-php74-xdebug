# Docker PHP v7.4 xdebug

Docker image to use php7.4 with xdebug using PHP Storm



This is a debugging usage example tested on Ubuntu, Windows and Mac  

### docker-compose-debug.yml

```yml
version: '3.5'
services:
  app:
    image: gbrayhan/php74-xdebug:v1.0
    ports:
      - "8000:80"
    working_dir: /srv/app
    volumes:
      - ./:/srv/app
    environment:
      XDEBUG_CONFIG: remote_host=docker.for.mac.localhost
      # XDEBUG_CONFIG: remote_host=localhost
      # XDEBUG_CONFIG: remote_host=host.docker.internal
    command: >
      bash -c "wget https://getcomposer.org/download/1.9.0/composer.phar
      && php composer.phar install --ignore-platform-reqs && /usr/sbin/apachectl -D FOREGROUND "
   
```
