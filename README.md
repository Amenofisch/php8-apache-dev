# php8-apache-dev

This is a simple template to get up and started quickly in the school in the programming lessons when learning SQL, PHP or HTML.  
Check out the list below to get more familiar with this simple template that cointains some basic stuff.

The default database is called `application` and is created automatically when starting the containers.

## Services:
- Apache with PHP 8.3
- PHPMyAdmin
- MariaDb 11 (Make sure port 3306 is not occupied on your machine, since we're passing MariaDb's port 3306 to our host machine's port 3306, so we can use SQL Clients)

## Getting started


### Prerequisites
- Docker Desktop installed

### Setup
1. Pull the repo to your local machine
2. Open the project using your favorite IDE.
3. Open a new terminal and run the following command: `docker compose up -d`
4. Now wait for the containers to start...
5. Once the containers started, you can check out the list below with the important URLs where you can open the Web server, PHPMyAdmin,...

## Usage
Before being able to do anything with the MariaDb database, you will have to start the containers.  
This is done using `docker compose up -d`, the same command as in the setup.  
Once you are done with using the containers, **don't forget to shut down the containers as they won't properly start after booting your computer**, to do so, just execute the following command inside the PHPStorm terminal: `docker compose down`

### URLs
- Apache: http://127.0.0.1:8085
- PHPMyAdmin: http://127.0.0.1:8090/phpmyadmin/
- MySQL on Port 3306

### Use MariaDB with PHPMyAdmin
Just simply open the URL listed above for PHPMyAdmin in your browser and you should be good to go.

### Use MariaDB with Shell
Run the following command to be able to execute commands directly in the MariaDb shell:   
`docker exec -it <CONTAINER_NAME> mariadb --user application -papplication`

To exit this shell you just have to type `exit`.

## Additional Infos

#### Database Password and Username
- Username: `application`
- Password: `application`

The `application` user has all permissions and can be accessed from every host/service.