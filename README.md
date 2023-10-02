# Laravel 10 Project with Docker Compose

This repository contains a basic setup for creating a Laravel 10 project using Docker Compose. This configuration includes Nginx as a web server, PHP 8.2 as the application server, and MySQL as the database.

## Setup Instructions

1. Run Docker Compose to build and start the containers:

    ```
    docker-compose up --build
    ```

2. Enter the PHP container:

    ```
    docker exec -it php-container-name bash
    ```

   Replace `php-container-name` with the name of your PHP container.


3. Use Composer to create a new Laravel project:

    ```
    composer create-project laravel/laravel example
    ```

4. Move all content from the "example" directory to the main directory:

    ```
    mv /var/www/html/example/{.,}* /var/www/html
    ```

5. Delete the "example" directory:

    ```
    rm -rf example
    ```

6. Access `localhost:8080` in your browser.
