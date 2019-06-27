# LEMP Stack

Docker running Nginx, PHP-FPM, Composer, MySQL and PHPMyAdmin.

## Clone the project

```sh
git clone https://github.com/siscopuig/docker-lemp.git
```

Go to the project directory :

```sh
cd docker-lemp
```

## Run the application

1. Copying the composer configuration file :

    ```sh
    cp web/app/composer.json.dist web/app/composer.json
    ```

2. Start the application :

    ```sh
    docker-compose up -d
    ```

    **View output from containers. Follow log output**

    ```sh
    docker-compose logs -f
    ```

3. Open your favorite browser :

    * [http://localhost:8000](http://localhost:8000/)
    * [http://localhost:8080](http://localhost:8080/) PHPMyAdmin (username: dev, password: dev)

4. Stop and clear services

    ```sh
    sudo docker-compose down -v
    ```

## Accessing MySQL Database

```sh
sudo docker exec -it mysql bash
```

and

```sh
mysql -u"$MYSQL_ROOT_USER" -p"$MYSQL_ROOT_PASSWORD"
```
