# docker-compose-symfony-mysql 

This project ensure docker environment for a symfony project with mysql database.

## Installation

You need to copy .env.prod or .env.dev to .env file.
Dev containing the development mode example, prod contain the production mode development environment setting example.
Check the .env file content especially the `PROJECT_NAME` variable!

## Docker Services

### mysql
* used image: [mysql:latest](https://hub.docker.com/_/mysql/tags)

### symfony
* used image: [php:8.2-fpm-alpine](https://hub.docker.com/_/php/tags?page=1&name=8.2-fpm-alpine)

### nginx
* used image: [nginx:1.21-alpine](https://hub.docker.com/_/nginx/tags?page=1&name=1.21-alpine)

### redis
* used image: [https://hub.docker.com/_/redis/tags?page=1&name=alpine](https://hub.docker.com/_/redis/tags?page=1&name=alpine)

## License

[MIT](https://choosealicense.com/licenses/mit/)