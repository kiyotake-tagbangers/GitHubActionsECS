# Run Locally

```shell
$ export JAVA_HOME=`/usr/libexec/java_home -v 11`

$ java -version
openjdk version "11.0.2" 2019-01-15
OpenJDK Runtime Environment 18.9 (build 11.0.2+9)
OpenJDK 64-Bit Server VM 18.9 (build 11.0.2+9, mixed mode)

$ ./mvnw clean package
$ ./mvnw spring-boot:run
```

# Build Image

```shell
$ ./mvnw spring-boot:build-image

$ docker image ls | grep spring                         
demo-spring-app                                                                    0.0.1-SNAPSHOT          f28972791845        40 years ago        257MB

$ docker run -p 8081:8081 demo-spring-app:0.0.1-SNAPSHOT
```

## Access

```shell
$ curl localhost:8081/
Hello World
```
