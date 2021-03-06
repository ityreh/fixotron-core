FIXotron Core
========

FIXotron Core is a Quarkus application and offers a REST API to run and manage FIX Sessions based on the FIX Engine implemented by QuickFix/J.

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

<hr>

![Overview][overview]

# Installation

You can pull the image from DokcerHub and distribute it in your containerized environment.

```bash
docker pull ityreh/fixotron-core
```

# Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## Manage Quarkus Extensions

You can obtain a list of the available extensions with:

```
mvn quarkus:list-extensions
```

If you want to enable extensions, you can use the following goal with a comma-separated list of the extensions you want to enable:

```
mvn quarkus:add-extension -Dextensions="hibernate-validator"
```

## Run & Test the Application

### Run (Development)

Run the application with the quarkus:dev goal.

```bash
mvn compile quarkus:dev
```

Access the application website via http://0.0.0.0:8080. You can get the API description through an OpenAPI specification via http://localhost:8080/openapi and you can test the API with Swagger UI via http://localhost:8080/swagger-ui.

### Test (UnitTests)

Run the UnitTests with the test goal.

```bash
mvn test
```

## Build an executable

### Build a native executable

Make sure that the environment variabel GRAALVM_HOME points to your GraalVM version. Use the package goal and the native profile to build a native executable.

```bash
mvn package -Pnative
```

### Build a container executable

The native executable is specific to your OS. To build an executable that runs in a container, use the package goal as follows.

```bash
mvn package -Dnative -Dquarkus.native.container-build=true
```

[overview]: ./doc/export/overview.png "Overview"
