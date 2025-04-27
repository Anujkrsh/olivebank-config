# OliveBank Configuration Server

This repository hosts the centralized configuration server for the OliveBank suite of applications. It manages and serves configuration properties across multiple microservices and environments, enabling dynamic updates without the need for redeployment.

## Overview

The OliveBank Config Server provides:

- Centralized and version-controlled external configuration
- Environment-specific configuration profiles (e.g., `dev`, `qa`, `prod`)
- Git-based configuration management
- Spring Cloud Config Server integration

## Repository Structure


Each YAML or properties file under `/config/` corresponds to a microservice and environment.

## Getting Started

### Prerequisites

- Java 17 or higher
- Maven 3.8 or higher

### Running the Server

Clone the repository and navigate to the project directory:

```bash
git clone https://github.com/Anujkrsh/olivebank-config.git
cd olivebank-config
```

Run the server using Maven:

```bash
mvn spring-boot:run
```

The configuration server will be available at:

```
http://localhost:8888
```

### Fetching Configuration

Microservices can fetch their configurations via:
```
GET http://localhost:8071/{application-name}/{profile}

```
### Technology Stack

- Java 17
- Spring Boot
- Spring Cloud Config Server
- Maven

Contributing
Contributions are welcome! Feel free to fork the repository and open pull requests for improvements or new features.