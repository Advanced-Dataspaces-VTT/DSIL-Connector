# Development Documentation

This section provides an overview of the development process for the VTT Data Space Connector. It includes the architectural description, interface specification, design description, and requirements for the connector. The goal of this section is to provide a comprehensive understanding of the development process, as well as the technical specifications for the connector.

[Document navigator](../docs/navigation_document.md)

## Architectural Description

The VTT Data Space Connector is based on the open-source implementation of the Data Space Connector provided by the International Data Spaces Association (IDSA). The IDSA Data Space Connector provides a secure and interoperable framework for exchanging data between organizations and data ecosystems, built on top of existing data exchange standards such as OPC-UA, and HTTP.

The VTT Data Space Connector extends the IDSA Data Space Connector by adding additional modules for authentication and authorization, data transformation and mapping, and data security. The authentication and authorization module is based on Spring Security, which provides support for various authentication mechanisms such as username and password, OAuth2, and OpenID Connect. The connector also integrates with Keycloak for identity and access control management, providing additional features such as single sign-on and fine-grained access control. The authorization module is based on access control policies defined using the JSON Web Token (JWT) standard.

The data transformation and mapping module provides support for transforming data between different formats and structures, using technologies such as XSLT and XPath. The data security module provides support for encrypting and decrypting data, as well as signing and verifying messages, using technologies such as XML Digital Signatures and Encryption.

The VTT Data Space Connector is designed to be highly configurable, allowing users to customize the connector to their specific needs. The connector supports various deployment models, including standalone deployment, container deployment, and cloud deployment. The connector is also designed to be highly scalable and fault-tolerant, with support for load balancing and clustering.


## Interface Specification

The interface specification provides a detailed description of the APIs and protocols used by the VTT Data Space Connector to communicate with other systems. This includes a description of the data formats used, as well as the authentication and authorization mechanisms employed by the connector.

The VTT Data Space Connector exposes several APIs and protocols to enable communication with other systems. These APIs and protocols are defined using industry-standard specifications such as REST, HTTP, and WebSockets. The connector also supports various data formats such as JSON, XML, and CSV, and provides data transformation and mapping capabilities to enable interoperability with different data models.

The authentication and authorization mechanisms employed by the VTT Data Space Connector are also defined in the interface specification. As mentioned earlier, the connector uses Spring Security and Keycloak to provide secure authentication and authorization. The APIs and protocols exposed by the connector are secured using access control policies defined using JWT tokens. This allows fine-grained control over access to resources and ensures that only authorized users and systems are able to interact with the connector.

In addition to the interface specification, the VTT Data Space Connector also provides a Swagger UI for easy exploration and testing of its APIs. The Swagger UI can be accessed via the URL https://localhost:8083/api/swagger-ui/index.html. To use the Swagger UI, you will need to enter a username and password. The default username is "admin" and the default password is "password".

The Swagger UI provides an interactive documentation of the connector's APIs, making it easier to understand and use the APIs. Users can explore the APIs, test them with sample requests, and view the responses. The Swagger UI also provides additional information such as data models and error messages.

Overall, the VTT Data Space Connector provides a comprehensive interface specification along with a user-friendly Swagger UI to enable seamless integration with other systems.

## Design Description

The design description provides a detailed description of the design and implementation of the VTT Data Space Connector. This includes a description of the software architecture, as well as the key design decisions and trade-offs made during development.

The VTT Data Space Connector is designed with a modular software architecture that enables it to be easily extensible and adaptable to various use cases. The connector's design is based on the IDSA Connector Framework, which defines a set of specifications and guidelines for developing secure and interoperable data space connectors. The VTT Data Space Connector employs the Microservices architectural pattern, which enables it to be divided into smaller, more manageable services that can be independently deployed and scaled. This design decision allows the connector to handle large volumes of data and provides flexibility in integrating with different data models and formats. The VTT Data Space Connector also uses a range of open-source technologies, including Spring Boot and Docker, to enable easy deployment and management of the connector. Overall, the VTT Data Space Connector's design is focused on flexibility, scalability, and security, making it well-suited for a variety of data space use cases.

The VTT Data Space Connector also employs a distributed architecture to improve fault tolerance and ensure high availability of data. The connector's architecture uses a combination of RESTful APIs, Kafka messaging, and Apache Cassandra database to enable distributed data processing and storage. This design decision allows the connector to operate in a highly available and fault-tolerant manner, ensuring that data is always accessible even in the event of failures.

In addition, the VTT Data Space Connector's design includes support for various data privacy and security measures. The connector uses encryption to secure data both in transit and at rest, and provides fine-grained access control to data resources using a combination of authentication and authorization mechanisms. The connector also supports data masking and anonymization to protect sensitive data and ensure compliance with privacy regulations.

Overall, the VTT Data Space Connector's design is focused on providing a flexible, scalable, and secure platform for enabling secure data exchange and collaboration in the context of data spaces.

## Requirements

The requirements section provides a comprehensive list of the functional and non-functional requirements for the VTT Data Space Connector. This includes a description of the use cases and scenarios supported by the connector, as well as the performance, scalability, and security requirements.

### Functional Requirements

* The VTT Data Space Connector shall support the exchange of data with other systems that comply with the IDSA Connector Framework.

* The VTT Data Space Connector shall support the exchange of data in various formats, including JSON, XML, and CSV.

* The VTT Data Space Connector shall provide data transformation and mapping capabilities to enable interoperability with different data models.

* The VTT Data Space Connector shall support the authentication and authorization mechanisms defined in the IDSA Connector Framework.

### Non-Functional Requirements

* The VTT Data Space Connector shall be scalable to handle large volumes of data.

* The VTT Data Space Connector shall be designed with security in mind and shall comply with relevant security standards.

* The VTT Data Space Connector shall be easy to deploy and manage using Docker and Docker Compose.

* The VTT Data Space Connector shall be performant, with low latency and high throughput.


### Performance Requirements

* The VTT Data Space Connector shall have low latency for data exchange operations.

* The VTT Data Space Connector shall support high throughput data exchange operations.

* The VTT Data Space Connector shall have minimal impact on the performance of connected systems.

### Scalability Requirements:

* The VTT Data Space Connector shall be designed with scalability in mind to handle increasing volumes of data.

* The VTT Data Space Connector shall be able to scale horizontally by adding more instances to the system.

* The VTT Data Space Connector shall support load balancing for distributing data exchange operations across multiple instances.

### Security Requirements:

* The VTT Data Space Connector shall use secure communication protocols to protect data in transit.

* The VTT Data Space Connector shall enforce role-based access control for managing access to data.

* The VTT Data Space Connector shall support encryption of data at rest.

* The VTT Data Space Connector shall be designed with security best practices in mind to minimize vulnerabilities and reduce the risk of attacks.

Proceed to [Testing Documentation](../docs/testing_documentation.md)