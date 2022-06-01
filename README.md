# data-access
Access related databases from Go using Docker, Docker Compose.

## Docker Container
```
# Starting Docker Container
$ docker-compose up -d

# Check Startup
$ docker ps -a

# Get into a Docker container
$ docker exec -it [CONTAINER ID] bash

# Connecting to mysql
$ mysql -h 127.0.0.1 -P 3306 -u root -p

# Create Database
mysql> create database recordings;

# Go to Database
mysql> use recordings;

# Add Table
mysql> source docker-entrypoint-initdb.d/create-tables.sql

# Check Table
mysql> select * from album;

# Exit mysql
mysql> \q

# Exit From Container
$ exit
```

## Run
```
$ DBUSER=root DBPASS=root go run .
```

## references
- [Tutorial: Accessing a relational database](https://go.dev/doc/tutorial/database-access)
 