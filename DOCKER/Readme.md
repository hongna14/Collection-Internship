# DOCKER
## Docker compose
 Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application’s services. Then, with a single command, you create and start all the services from your configuration.
1. Installation
[Install the Compose standalone](https://docs.docker.com/compose/install/other/)
2. Config docker-compose.yml and run *'docker-compose up'*
```yml
services:
    postgresql_database:
        image: postgres:latest
        container_name: some-postgres
        environment:
            - POSTGRES_USER=postgres
            - POSTGRES_PASSWORD=postgres
        ports: 
            - "5432:5432"
        restart: unless-stopped
        volumes: 
            - database-data:/var/lib/postgresql/data/
volumes:
    database-data:
```
## Postgres Image
PostgreSQL, often simply "Postgres", is an object-relational database management system (ORDBMS) with an emphasis on extensibility and standards-compliance. As a database server, its primary function is to store data, securely and supporting best practices, and retrieve it later, as requested by other software applications, be it those on the same computer or those running on another computer across a network (including the Internet). It can handle workloads ranging from small single-machine applications to large Internet-facing applications with many concurrent users. Recent versions also provide replication of the database itself for security and scalability

## Note
```
Change owner  root --> user: chown $USER:$USER
Docker informations: docker info 
Contaners in docker: docker ps
Contaners is running: docker ps -a
Delete all containers: docker container prune -f
Docker cp: docker cp [OPTIONS] SRC_PATH|- CONTAINER:DEST_PATH
```