# mvn-nvm-build Base Image #
[![Build Status](https://travis-ci.org/clusterfk/docker-base-images.svg?branch=master)](https://travis-ci.org/clusterfk/docker-base-images)

A simple base image with a `maven:3-jdk-11` base and `nvm` ([Node Version Manager](https://github.com/nvm-sh/nvm)) installed.

```sh
docker pull clusterfk/mvn-nvm-build
```

## Example Usage ##

In your current working directory:

```sh
DESIRED_NODE_VERSION=6.9.1

cat > my-build-script.sh <<- EOM
source /root/.bashrc # load nvm aliases
nvm install ${DESIRED_NODE_VERSION}
nvm use ${DESIRED_NODE_VERSION}
# Do other awesome stuff here
EOM

chmod +x my-build-script.sh

container=build-docker

docker run --name ${container} -d -it -v ${PWD}:/usr/app/ clusterfk/mvn-nvm-build /bin/bash
docker exec -it ${container} /bin/bash "/usr/app/my-build-script.sh"
```

**Output**:
```sh
Downloading and installing node v6.9.1...
Downloading https://nodejs.org/dist/v6.9.1/node-v6.9.1-linux-x64.tar.xz...
######################################################################## 100.0%
Computing checksum with sha256sum
Checksums matched!
Now using node v6.9.1 (npm v3.10.8)
```

## Building ##

* Built with [fabric8io docker-maven-plugin](https://github.com/fabric8io/docker-maven-plugin/).

```sh
mvn clean package
```
