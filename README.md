# tech-challenge-time
This repository contains the docker-compose which will startup all the dockers needed for tech-challenge-time.

## Execute
docker and docker-compose (compatible with version 3.1) must be installed.
For the application to start simply clone this repository and execute the following command in the root of the cloned repository.
```sh
docker-compose up
```
This will spin up two accessible apps at the following ports by default:
GraphQL backend API:
```sh
http://localhost:8080/query
```
Web frontend:
```sh
http://localhost:5000
```

The database will generate a postgres_data/ folder wherever docker-compose is executed that stores the volume of the database.

## Dependencies
This web application is composed of 3 different dockers. You can find more information on each link
* [frontend-tech-challenge-time](https://github.com/OscarClemente/frontend-tech-challenge-time): The frontend of the web app. Based on svelte + urql.
* [backend-tech-challenge-time](https://github.com/OscarClemente/backend-tech-challenge-time): The backend of the web app. Based on Go + gqlgen + go-pg.
* [postgres](https://hub.docker.com/_/postgres/): The official docker of the postgreSQL database.

## Integration tests
Inside the integration_tests/ folder there is another docker-compose description file intended to be used for integration testing.
The integration tests are available at [karate-tech-challenge-time](https://github.com/OscarClemente/karate-tech-challenge-time).
They are intended to test the backend GraphQL API along with the DB. You can refer to its repo for more information.
