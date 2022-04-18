# Docker For Development Example Application

- Example application from blog post: https://www.freecodecamp.org/news/author/sesigl/
- Demo Application copied and modified from: https://github.com/spring-guides/gs-accessing-data-rest.git

## Useful Commands

### Run Integration Tests Using a Dockerized MySQL Database
`./mvnw clean test`

### Build a Local Application Docker Container
`./mvnw compile jib:dockerBuild`

### Start A MySQL Database
`docker run --rm -v "$PWD/data":/var/lib/mysql --name mysql -e MYSQL_ROOT_PASSWORD=admin-password -e MYSQL_DATABASE=my-database -p 3306:3306 mysql:8.0.28-debian`

### Start The Dockerized Application
`docker run --net=host my-docker-image`
