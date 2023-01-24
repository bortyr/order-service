# Generate Spring Boot Project

```
openapi-generator generate -g spring -i openapi.yaml -c conf.json -o order-service 
```

# Start project in generated directory

```sh
mvn package spring-boot:run
```
