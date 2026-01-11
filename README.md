# Splitit
A little web app to split holidays expenses

## Project Structure

This is a multi-module Maven project with the following structure:

```
splitit/
├── pom.xml                          # Root POM (splitit-root)
└── splitit-web/                     # Quarkus web application module
    ├── pom.xml
    └── src/
        ├── main/
        │   ├── java/
        │   │   └── org/asymetrik/splitit/
        │   │       └── GreetingResource.java
        │   └── resources/
        │       └── application.properties
        └── test/
            └── java/
                └── org/asymetrik/splitit/
                    └── GreetingResourceTest.java
```

## Technology Stack

- **Java**: 25
- **Framework**: Quarkus 3.30.6
- **Build Tool**: Maven 3.9+
- **Group ID**: org.asymetrik.splitit
- **Modules**:
  - `splitit-root` - Root parent module
  - `splitit-web` - Quarkus web application

## Building the Project

To build the entire project:

```bash
mvn clean install
```

To skip tests during build:

```bash
mvn clean install -DskipTests
```

## Running the Application

### Development Mode

To run the Quarkus application in development mode (with hot reload):

```bash
cd splitit-web
mvn quarkus:dev
```

The application will be available at: http://localhost:8080

### Testing the Application

To run tests:

```bash
mvn test
```

### Sample Endpoint

Once running, you can test the sample endpoint:

```bash
curl http://localhost:8080/hello
```

Expected response: `Hello from Splitit!`

## Development

This project uses Quarkus, which offers:
- Fast startup time
- Live reload during development
- Optimized for containerization
- Reactive and imperative programming models

## Requirements

- Java 25 or higher
- Maven 3.9.12 or higher
