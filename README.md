## This is a simple CRUD API for todos.

I built it to learn the process of deploying a dotnet core application to heroku using a docker container.

You can test the API using Postman at [https://todo-api-docker.herokuapp.com/api/todo](https://todo-api-docker.herokuapp.com/api/todo).

The process for deployment to heroku is as follows:

- run `dotnet publish -c Release -o out`
- run `docker build -t [DOCKER_IMAGE_NAME] -f ./Dockerfile.web .`
- run `docker tag [DOCKER_IMAGE_NAME] registry.heroku.com/[HEROKU_APP_NAME]/web`
- run `heroku container:push web -a [HEROKU_APP_NAME]`
- run `heroku open -a [HEROKU_APP_NAME]`

This project uses Entity Framework In Memory Storage.