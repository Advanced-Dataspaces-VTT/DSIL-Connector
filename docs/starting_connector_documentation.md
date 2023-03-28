# Starting The VTT connector

[Document navigator](../docs/navigation_document.md)

## Configuring The Identity and Access Control Mechanism
The VTT connector is preconfigured to run with either Spring Boot Security or Keycloak, by default the Spring Boot Security is selected. To change this you can navigate to the [application.properties](Connector/src/main/resources/application.properties) file and locate the following two lines:
```
spring.security.enabled=true
keycloak.enabled=false
```
(Note: only have one value should be set as true)

## Starting The Connector With The Chosen Identity and Access Control Mechanism

The VTT connector can be run with either Docker run or docker compose, please not everything is already preconfigured so if you deviate from the guide please ensure you cascade the adjustments throughout the application.

(Note: the chosen Identity and Access Control Mechnaism does not have any affect on this step)

Docker run command
```
sudo docker build -t dsca .
sudo docker run --publish 8083:8081 --name connectorc dsca
```

Docker compose command
```
sudo docker compse up --build -d
```

Successfully running these commands will create two containers
* "connectorc"
* "postgres-connectorc"