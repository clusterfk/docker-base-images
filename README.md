<img src="https://i.ibb.co/CmyCwp9/Webp-net-resizeimage-7.png" alt="91a16b7b-336f-402f-a78b-d194550da559" border="0"></a><br />

# clusterfk Docker Base Images #

A maven build parent holding various docker base images.

* [mvn-nvm-build](mvn-nvm-build/README.md) - [![Build Status](https://travis-ci.org/clusterfk/docker-base-images.svg?branch=master)](https://travis-ci.org/clusterfk/docker-base-images)

## Building ##

* Built with [fabric8io docker-maven-plugin](https://github.com/fabric8io/docker-maven-plugin/).

```sh
mvn clean package
```

## Releasing ##

```sh
mvn release:perform
```
