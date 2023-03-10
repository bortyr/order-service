# Order Service REST API with OpenAPI Docs

## Getting started

Change into directory of project from the previous assignment and launch it with IntelliJ IDEA.

```sh
cd RabbitMQProject
```

Start RabbitMQ as docker container:

```sh
docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3.11-management
```

Launch both of services:

1. Order Service (REST Service) -> on port 8090
2. Order Events Processor (Receiver of RabbitMQ messages) -> on port 8070

![IntelliJ_Image](./contents/img1.png)

Launch our OpenAPI documentation with SwaggerUI.

If it's not present, generate it:
```
openapi-generator generate -g spring -i openapi.yaml -c conf.json -o order-service 
```

Run the service in the generated directory. It will start on port 8080
```sh
mvn package spring-boot:run
```
