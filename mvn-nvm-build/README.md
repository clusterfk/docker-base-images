# mvn-nvm-build Base Image #
[![Build Status](https://travis-ci.org/clusterfk/docker-base-images.svg?branch=master)](https://travis-ci.org/clusterfk/docker-base-images)

A simple base image with a `maven:3-jdk-11` base and `nvm` ([Node Version Manager](https://github.com/nvm-sh/nvm)) installed.

## Example Usage ##

In your current working directory:

```sh
echo "echo hello" > my-build-script.sh && chmod +x my-build-script.sh

container=hello_world

docker run --name ${container} -d -it -v ${PWD}:/usr/app/ clusterfk/mvn-nvm-build
docker exec -it ${container} /bin/bash "/usr/app/my-build-script.sh"
```

## Building ##

* Built with [fabric8io docker-maven-plugin](https://github.com/fabric8io/docker-maven-plugin/).

```sh
mvn clean package
```
