# Ticket

Access to data base in memory

H2 DATABASE
============
http://localhost:80801/h2-console/
JDBC URL: jdbc:h2:mem:testdb user:     sa password: password

show the swagger

http://localhost:8080/swagger-ui.html

### Versioning

* **Version** 1.0

* **LOG classes**

* **PMD changes**
    - All

* **Checkstyle**
    - All

* **FindBugs**
    - All

* **Others**
    - Lombok annotations:
        - TicketRequest.java
        - TicketResponse.java


#### Last modification date:

#### Change history


### Endpoints

> /api/v1/operation/ticket/insert (POST)

#### Request data
````
This json is used to insert the values in data base.
````

```json
{
  "fechaSalida": "11/06/2021",
  "fechaLlegada": "11/06/2021",
  "origen": "CDMX",
  "destino": "Tijuana",
  "nombre": "Raul Gutierrez",
  "edad": "32",
  "equipaje": false,
  "precio": "1000.00",
  "horaSalida": "11:10",
  "horaLlegada": "13:10"
}
```

#### Response
```
> Status: 200, OK
```

> /api/v1/operation/ticket/id?id=X (GET)

### Response
```json
{
  "itineraryID": 1,
  "fechaSalida": "2021-06-11",
  "fechaLlegada": "2021-06-11",
  "origen": "CDMX",
  "destino": "Tijuana",
  "nombre": "Raul Gutierrez",
  "edad": 32,
  "equipaje": false,
  "precio": 1000,
  "horaSalida": "11:10:00",
  "horaLlegada": "13:10:00"
}
```

## Built With
* Maven
* Spring
* SpringBoot

### Prerequisites
You need to have installed:

- Logged in the citi banamex intranet
- Java 1.8
- Maven
- Spring Tool Suite or IntelliJ IDE
- Lombok installed inside IDE

## Deployment

```console
	$ mvn spring boot:run
```
Or from STS right click on the project -> Run As -> Spring Boot App

- On STS(Spring Tool Suite) right click on the project  > Run As >
  JUnit Test
- Or for **debugging** right click on the project  > Debug As > JUnit Test

For run a unique test just go to the src/test/java package that is the test and select the test by clicking on the name of it -> Right click --> Run As -> JUnit test

For run a unique test in debug mode just go to the src/test/java package that is the test and select the test by clicking on the name of it -> Right click --> Debug As -> JUnit test

To run this microservice in local mode use the ```bootstrap.yml``` file.

Be sure to not commit this changes to BitBucket.


To generate a google standard check-style html site.


It is divided in two categories:

1. Project Information

    - Provides an overview of the various documents and links that are part of this project's general information.

2. Project Reports

    - Provides an overview of the various reports that are automatically generated by Maven.

The site is generated on the project folder: target > site > index.html


	$ mvn clean install site


Sonar is an open source platform used by development teams to manage source code quality.


	$ mvn -X jacoco:prepare-agent clean test sonar:sonar

Or from STS rigth click on the project -> Run As -> Maven Build... -> Goals: sonar:sonar -> Run

In the lasts lines of the console there is a link, copy and paste it on any web browser to see the report.