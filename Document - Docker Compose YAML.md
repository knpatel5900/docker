# Documentation Referred:

https://docs.docker.com/compose/install/

# Commands used for Installing Docker Compose in Linux:

    curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
    chmod +x /usr/local/bin/docker-compose
    
# Sample Wordpress Compose file used:

# Step 1: Create a new directory named wordpress

    mkdir wordpress
    cd wordpress

# Step 2: Create a file named docker-compose.yml and store the below snippet there:

    version: '3.3'

    services:
       db:
         image: mysql:5.7
         volumes:
           - db_data:/var/lib/mysql
         restart: always
         environment:
           MYSQL_ROOT_PASSWORD: somewordpress
           MYSQL_DATABASE: wordpress
           MYSQL_USER: wordpress
           MYSQL_PASSWORD: wordpress

         wordpress:
           depends_on:
             - db
           image: wordpress:latest
           ports:
             - "8000:80"
           restart: always
           environment:
             WORDPRESS_DB_HOST: db:3306
             WORDPRESS_DB_USER: wordpress
             WORDPRESS_DB_PASSWORD: wordpress
             WORDPRESS_DB_NAME: wordpress
           volumes:
               db_data: {}
# Build Commands 
# start Docker Compose

    docker-compose up -d

# Bring Down application started via Docker Compose

    docker-compose down
