# circleci-build
Build a docker image with CircleCi. Based on the CircleCI doc [Hello World](https://circleci.com/docs/2.0/hello-world/) and the blog [Using CircleCi Workflows to Replicate Docker Hub Automated Builds](https://circleci.com/blog/using-circleci-workflows-to-replicate-docker-hub-automated-builds/).

## Setup
- create new github repo `circleci-build` and copy these files into the repo
- build and run docker container locally
```
docker build --tag goapp .
docker run goapp
hello world
```
- login do Docker Hub and create a new repository `circleci-build`
- push local image to `mydockerhub-user/circleci-build`
```
docker login
docker tag goapp mydockerhub-user/circleci-build:initialbuild
docker push mydockerhub-user/circleci-build
docker run mydockerhub-user/circleci-build
hello world
```

## Build app locally (optional)
```
go build .
go run .