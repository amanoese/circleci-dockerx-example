circleci-dockerx-example
---

[![CircleCI](https://circleci.com/gh/amanoese/circleci-dockerx-example/tree/master.svg?style=svg)](https://circleci.com/gh/amanoese/circleci-dockerx-example/tree/master)

This Repository is example what build Docker container for multi-architecture using docker buildx.  
After That Push Dockerhub.

circleciでdocker buildxを利用してマルチアーキテクチャ対応のコンテナをビルドする例です。  
DockerHubにpushします。


## Local init

```bash
$ docker buildx ls
$ docker buildx create --use --name xbuilder
$ docker buildx inspect --bootstrap
$ docker buildx ls
```

## Local push 

```bash
$ docker buildx build --platform linux/amd64,linux/arm64 -t <<DOCKER_NAME>>/dockerx-ex --push .
```
### Using CircleCI CLI

```bash
$ circleci local execute -e DOCKER_USER=<<DOCKER_NAME>> -e DOCKER_PASS=<<DOCKERHUB_ACCESS_TOKEN>>
```

