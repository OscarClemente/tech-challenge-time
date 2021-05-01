# tech-challenge-time
This repository contains the docker-compose which will startup all the dockers needed for tech-challenge-time.

## Execute
docker and docker-compose (compatible with version 3.1) must be installed.
For the application to start simply clone this repository and execute the following command in the root of the cloned repository.
```sh
docker-compose up
```
This will generate a postgres_data/ folder wherever docker-compose is executed that stores the volume of the database
## Dependencies
This web application is composed of 3 different dockers. You can find more information on each link
* [frontend-challenge-time](https://github.com/OscarClemente/frontend-tech-challenge-time): The frontend of the web app. Based on svelte + urql.
* [backend-challenge-time](https://github.com/OscarClemente/backend-tech-challenge-time): The backend of the web app. Based on Go + gqlgen + go-pg.
* [postgres](https://hub.docker.com/_/postgres/): The official docker of the postgreSQL database.
