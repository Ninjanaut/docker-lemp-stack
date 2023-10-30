Docker LEMP stack
=================

This project contains a docker compose file that will create three containers

* Nginx
* PHP
* MySQL

## Requirements

- Git
- Docker engine

## Windows Installation

- Install [Git](https://git-scm.com/) or any git related client
- Clone the project to your local developer machine workspace using [Git clone](https://github.com/git-guides/git-clone) command
- Install [Docker](https://www.docker.com/get-started/)
- Open command prompt as administrator
    - Switch to the project root directory
    - Run the following command that will download all the files and create the containers

            docker compose up -d

- Copy PHP application to the `src/` folder
- Open `localhost` address in web browser
- To get MySQL server IP address
    - Copy container id of the MySQL container

            docker ps -a

        - and run the following command that will return IP address

                docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <container id>
    