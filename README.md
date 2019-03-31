# microprofile-examples [![Build Status](https://travis-ci.org/daggerok/microprofile-examples.svg?branch=master)](https://travis-ci.org/daggerok/microprofile-examples)
MicroProfile examples

## Micro Profiles

see pom.xml in [here](./maven-profiles)

## OpenLiberty

### maven

#### zip

_build, run and test_

```bash
./mvnw -f openliberty-maven-zip/pom.xml package liberty:start

http :9080/app1/
http :9080/app1/v1/properties

./mvnw -f openliberty-maven-zip/pom.xml liberty:stop liberty:clean-server
```

#### zip (docker)

_build_

```bash
./mvnw -f openliberty-maven-zip/pom.xml clean package
docker build -t openliberty-maven-zip -f openliberty-maven-zip/Dockerfile openliberty-maven-zip
```

_run_

```bash
docker run --name app --rm -p 9080:9080 -p 9443:9443 openliberty-maven-zip
```

_test_

```bash
http :9080/app1/
http :9080/app1/v1/properties
```

#### jar

_build_

```bash
./mvnw -f openliberty-maven-jar/pom.xml clean package
docker build -t openliberty-maven-jar -f openliberty-maven-jar/Dockerfile openliberty-maven-jar
```

_run_

```bash
docker run --name app --rm -p 9080:9080 -p 9443:9443 openliberty-maven-jar
```

_test_

```bash
http :9080/app2/
http :9080/app2/v1/properties
```

### gradle

#### zip

_build, run and test_

```bash
./gradlew -b openliberty-gradle-jar/build.gradle libertyStart

http :9080/app3/
http :9080/app3/v1/
http :9080/app3/v1/hoy

./gradlew -b openliberty-gradle-jar/build.gradle libertyStop
```

links:

* [GitHub: eclipse/microprofile-samples](https://github.com/eclipse/microprofile-samples/blob/master/pom.xml)

other JakartaEE / MicroProfile repositories:

* [GitHub: daggerok/java-mp-tomtribe-tomee-maven-example](https://github.com/daggerok/java-mp-tomtribe-tomee-maven-example)
* [GitHub: daggerok/java-mp-smallrye-example](https://github.com/daggerok/java-mp-smallrye-example)
* [GitHub: daggerok/java-mp-openliberty-gradle-example](https://github.com/daggerok/java-mp-openliberty-gradle-example)
* [GitHub: daggerok/meecrowave-example](https://github.com/daggerok/meecrowave-example)
* [GitHub: daggerok/java-ee-microservices](https://github.com/daggerok/java-ee-microservices)
* [GitHub: daggerok/payara-micro-gradle-plugin-build-script](https://github.com/daggerok/payara-micro-gradle-plugin-build-script)
* [GitHub: daggerok/payara-micro-gradle-no-plugin](https://github.com/daggerok/payara-micro-gradle-no-plugin)
* [GitHub: daggerok/payara-micro-example](https://github.com/daggerok/payara-micro-example)
* [GitHub: daggerok/thorntail-example](https://github.com/daggerok/thorntail-example)
* [GitHub: daggerok/wildfly-swarm-microservice](https://github.com/daggerok/wildfly-swarm-microservice)
* [GitHub: daggerok/wildfly-swarm-jgroups-chat](https://github.com/daggerok/wildfly-swarm-jgroups-chat)
* [GitHub: daggerok/java-ee-examples](https://github.com/daggerok/java-ee-examples)

