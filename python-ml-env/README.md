# python-ml-env Base Image #
[![Build Status](https://travis-ci.org/clusterfk/docker-base-images.svg?branch=master)](https://travis-ci.org/clusterfk/docker-base-images)

A simple base image with a `python:3.7.2-slim` and some relevant ML packages.

```sh
docker pull clusterfk/python-ml-env
```

## Building ##

* Built with [fabric8io docker-maven-plugin](https://github.com/fabric8io/docker-maven-plugin/).

```sh
mvn clean package
```
