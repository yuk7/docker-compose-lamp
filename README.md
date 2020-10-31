# Docker-Compose LAMP Test Environment

## Services
* PHP7.4 with Apache :80 port
* MariaDB :3306 port
* phpMyAdmin :4000 port

## Run
```bash
docker-compose up -d
```

## Directory Specification
```
.
├── docker-compose.yml  : docker-compose file
├── htdocs  :document root
├── data  :persistence directory
│   └── mysql  :persistence data for database
└── services  :service configuration directory
    ├── mariadb
        └── initdb.d  :put sql file for db initialization
    └── php
        ├── Dockerfile  :php service build file
        └── php.ini  :php configuration file
```