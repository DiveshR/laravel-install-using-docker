<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>



## Laravel Setup using Docker and sail

### Sail on Mac

`````
curl -s "https://laravel.build/laravel-app-using-docker" | bash

cd laravel-app-using-docker
./vendor/bin/sail up 
To run laravel project using sail

Laravel Sail is a light-weight command-line interface for interacting with Laravel's default Docker development environment. Sail provides a great starting point for building a Laravel application using PHP, MySQL, and Redis without requiring prior Docker experience.

https://laravel.com/docs/10.x/sail


http://localhost/
``````

In docker-compose.yml

Add above code to setup phpmyadmin in docker

````php
    phpmyadmin:
        depends_on:
            - mysql
        image: phpmyadmin/phpmyadmin
        environment:
            - PMA_HOST=mysql
            - PMA_PORT=3306
        networks:
            - sail
        ports:
            - 8001:80

`````
After Adding mysql docker config down sail

````
./vendor/bin/sail up 
`````
Again Sail Up

```
./vendor/bin/sail up 
````
http://localhost:8001/# laravel-install-using-docker
