# Order Service REST API with OpenAPI-Generator and Spring Boot

## Generate Spring Boot Project

```
openapi-generator generate -g spring -i openapi.yaml -c conf.json -o order-service 
```

## Start project in generated directory

```sh
mvn package spring-boot:run
```

## Start RabbitMQ

```
docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3.11-management
```
