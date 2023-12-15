## how to connect php with mysql in codespace using docker compose

<hr>

![image](https://github.com/Abidali08/MYSQL_PHP_DOCKER/assets/49807758/b49f5052-0542-4901-bcee-bb28e2fc52df)

### Explanation:

- This Docker Compose file defines three services: www, db, and phpmyadmin.
- The www service uses the php:apache Docker image, syncs the project directory to the container's web directory, and exposes ports 80 and 433.
- The db service uses the mysql:latest image, sets up environment variables for MySQL configuration, and syncs a local directory (./db) with the container for persistent SQL files.
- The phpmyadmin service uses the phpmyadmin/phpmyadmin image, exposes port 8001, and specifies the MySQL host and port for connection.


<hr>

![image](https://github.com/Abidali08/MYSQL_PHP_DOCKER/assets/49807758/19dd3627-e72c-45f4-845b-e33e6eb5b5dd)

### Explanation:

- The PHP script establishes a connection to a MySQL database using the provided credentials ('db', 'phpdocker', 'password', 'php_docker').
- It selects all records from a table named php_docker_table.
- The fetched data is then echoed in an HTML format, displaying the title, body, and date_created fields.
- Each record is separated by an hr tag.

#### Overall, this setup uses Docker Compose to define and run three services (web server, database, and phpMyAdmin) and a PHP script to query and display data from a MySQL database.

### For Execute this code run this command in terminal of Codespace
- docker-compose up

### For Stop execution run this
![image](https://github.com/Abidali08/MYSQL_PHP_DOCKER/assets/49807758/2606099f-ded3-40e1-bd5c-42655867f687)

- docker-compose up

### Any case of this error 

![image](https://github.com/Abidali08/MYSQL_PHP_DOCKER/assets/49807758/5296a7f0-b838-4bc9-911e-7949201c06bf)

- Excute this command in apache image
- ![image](https://github.com/Abidali08/MYSQL_PHP_DOCKER/assets/49807758/efc7578a-41a4-4e31-957a-6f5b20ba338a)

  ## docker-php-ext-install mysqli

  - after excution of above command restart the container 
