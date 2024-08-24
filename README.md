# springboot3-soap-server

This application is a modern variant of a demo by Java Techie (https://www.youtube.com/watch?v=ceSqN3CWd14). The important changes are:

- Spring Boot 2 -> 3.x
- XJC plugin 1.6 -> 3.x
  - schemaDirectory -> sources
  - XSD in its own directory under properties (prevents XJC errors)
- Java 8 -> 17 
- Test messages added
- Location generated sources: /src -> /target

# view wsdl

Spring Boot generates a WSDL based on the XSD.
Url: http://localhost:8080/ws/loanEligibility.wsdl

# testberichten

The http-tests directory contains two XML test messages. 
These messages can be send to a running application with file tests.http. 
In IntelliJ Ultimate, the tests can be started with the built-in HTTP client using the green arrow.

From the CLI, the test messages can be sent as requests using curl:
```curl
curl -v -X POST -H "Content-Type: text/xml;charset=UTF-8" --data @http-tests/approved.xml http://localhost:8080/ws
curl -v -X POST -H "Content-Type: text/xml;charset=UTF-8" --data @http-tests/denied.xml http://localhost:8080/ws
```