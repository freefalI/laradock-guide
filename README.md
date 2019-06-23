# Laradock environment setup Manual  with Laravel) 

##  Requirements
- Git
- Docker
- Docker-Compose
- Composer (optional)

##  How to create laravel + laradock project 
### 1. if you already have not php project

    mkdir myproject && cd mkdir myproject

Install laradock:

    git clone https://github.com/laradock/laradock.git

Install laravel:

    composer create-project --prefer-dist laravel/laravel project

then

    cd laradock && mv env-example .env

in env change:

    APP_CODE_PATH_HOST=../project

run workspace

    sudo docker-compose up -d nginx mysql 

get access to terminal

    sudo docker-compose exec workspace bash


If necessary change permission on storage folder:

    chmod -R 777 storage/logs




##  2. if you already have php project

    composer install
    git submodule add https://github.com/Laradock/laradock.git
    cd laradock && cp env-example .env
    sudo docker-compose up -d nginx mysql 
get access to terminal

    sudo docker-compose exec workspace bash
    
other

    php artisan key:generate
    

### Run and stop workspace 

run

    docker-compose up -d nginx mysql
    
stop

    docker-compose stop  

