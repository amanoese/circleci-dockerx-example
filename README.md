circleci-dockerx-example
---

[![CircleCI](https://circleci.com/gh/amanoese/circleci-dockerx-example/tree/master.svg?style=svg)](https://circleci.com/gh/amanoese/circleci-dockerx-example/tree/master)

This Repository is example what build Docker container for multi-architecture using docker buildx.
After That Push Dockerhub.

circleciでdocker buildxを利用してマルチアーキテクチャ対応のコンテナをビルドする例です。
一応DockerHubにpushします。


## Local Init

```bash
docker buildx ls
docker buildx create --use --name xbuilder
docker buildx inspect --bootstrap
docker buildx ls
```

