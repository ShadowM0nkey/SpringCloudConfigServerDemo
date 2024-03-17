# SpringCloudConfigServerDemo
Demo program for the Spring Cloud Config Server using local (aka native) config files as opposed to remote git repositories. Includes both the server and client.

Derived from StackOverflow thread that included a lot of examples on GitHub but oddly (frustratingly) missing a full-fledged demo for the native mode: https://stackoverflow.com/questions/54557032/spring-cloud-config-server-configuration-with-local-repository

* Start Config & Client Servers using `./gradlew bootRun`
* Test Config Server
```
$ curl localhost:8888/aService/test
{"name":"aService","profiles":["test"],"label":null,"version":null,"state":null,"propertySources":[{"name":"classpath:/config/aService/aService-test.properties","source":{"service":"aServiceTest","a":"2","name":"Aservice"}}]}
```
* Test Client Server
```
$ curl localhost:8080/name
Aservice
```
