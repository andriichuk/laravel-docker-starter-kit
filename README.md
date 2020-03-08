### Laravel Docker Local Environment

#### Services

* [NGINX](https://hub.docker.com/_/nginx) (alpine)
* [MySQL 5.7](https://hub.docker.com/_/mysql)
* [PHP 7.4.3](https://hub.docker.com/_/php)
* PHP Packages
    * [Laravel](https://laravel.com/docs/7.x)
    * [Composer](https://hub.docker.com/_/composer)

#### Configuration

1. Create `.env` file:

    ```bash
    cp .env.example .env
    ```

2. Add `APP_USER` variable:
    ```ini
    APP_USER=serge
    ```
   
3. Fill `DB_*` credentials:

    ```ini
    DB_CONNECTION=mysql
    DB_HOST=app-storage
    DB_PORT=3306
    DB_DATABASE=laravel
    DB_USERNAME=laravel
    DB_PASSWORD=secret
    ```
   
4. Build Docker environment:

    ```bash
    docker-compose build
    ```

5. Run Docker environment:

    ```bash
    docker-compose up
    ```
   
6. Add site domain to `/etc/hosts` file (Linux):

```text
127.0.0.1 local-app.com
```
