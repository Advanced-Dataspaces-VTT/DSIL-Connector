# Installation Procedures

[Document navigator](../docs/navigation_document.md)

## Prerequiesites

The VTT connector has been tested on Windows, Macentosh, and Linux distributions however we suggest the following base prerequesetis.


|Operating system||
|----------------|--------|
| Distributor ID | Ubuntu |
| Description | Ubuntu 22.04.2 LTS |
| Release | 22.04 |
| Codename | jammy |


|Docker version||
|---|---|
|Version|23.0.1|
|API version|1.42|
|Go version|go1.19.5|
|Git commit|a5ee5b1|
|Built|Thu Feb  9 19:47:01 2023|
|OS/Arch|linux/amd64|
|OS/Context|default|


Docker compose version
```
Docker Compose version v2.15.1
```

Git version
```
git version 2.34.1
```

Port allocation
| Owner | External Port | Internal Port | Container Name |
|-------|---------------|---------------|----------------|
| IDS-Test-Bed | 8080 | 8081 | connectora |
| IDS-Test-Bed | 8081 | 8081 | connectorb |
| VTT-Connector | 8083 | 8081 | connectorc |
| IDS-Test-Bed | 5432 | 5432 | postgres-ids-test-bed |
| VTT-Connector | 5439 | 5432 | postgres-connectorc |
| IDS-Test-Bed |  |  | broker-fuseki |
| IDS-Test-Bed | 80 | 80 | omejdn |
| IDS-Test-Bed | 443 | 443 | omejdn |
| IDS-Test-Bed |  |  | omejdn-ui |
| IDS-Test-Bed |  |  | broker-core |
| IDS-Test-Bed |  |  | omejdn-server |
| IDS-Test-Bed |  |  | broker-reverseproxy |
| OPCUA-Server |  |  |  |


## Github Reposiory

Run the following command to clone the repository
```
git clone https://github.com/Advanced-Dataspaces-VTT/DSIL-Connector
```

The cloned repository should look as follows
```
---------
Run Tree command to show the parent directories in the root directory
---------
```

As displayed above is the VTT connector parent directory and the IDS-Test-Bed parent directory. The reason for inlcudeing the IDS-Test-Bed was to demonstrate how VTT had tested its connector with the industry standards provided by the IDS-Test-Bed, VTT cloned the IDS-Test-Bed repository adjusted the Newman test along with the default postman collection to use their connector instead of the connector "connectorb", the test now works by communicating from VTT connector "connectorc" to IDS-Test-Bed connector "connectora", we will explain later how to perform this test yourself, for it is not important.



### Interacting With The Connector
VTT has created three preconfigured postman collections which can be found under the "postman" directory. You must use the correct postman collection for the chosen Identity and Access Control Mechanism

If Keycloak is enabled (keycloak.enabled=true) then you should use the postman collection and environment variables found under the Keycloak directory of the postman directory

If Spring is enabled (spring.security.enabled=true) then you should use the postman collection and environment variables found under the Spring directory of the postman directory. Note there is also a Spring OPCUA collection we will go into more detail about that later, for now lets focus on the Spring and Keycloak usage.

Next steps:

[Running the VTT connector with Spring](../docs/spring_documentation.md)

[Running the VTT connector with Keycloak](../docs/keycloak_configuration.md)

[Running the VTT connector with OPCUA](../docs/opcua_configuration.md)

[Testing the VTT connector with the IDS-Test-Bed](../docs/opcua_configuration.md)

[Troubleshooting]()


