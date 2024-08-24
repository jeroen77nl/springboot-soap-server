# springboot-soap-server

Deze applicatie is een moderne variant van een demo van Java Techie (https://www.youtube.com/watch?v=ceSqN3CWd14).
Belangrijkste aanpassingen:
- spring boot 2 -> 3.x
- xjc plugin 1.6 -> 3.x
  - schemaDirectory -> sources
  - xsd een eigen directory onder properties (voorkomt xjc fouten)
- java 8 -> 17
- testberichten toegevoegd

# wsdl

Spring Boot maakt op basis van de xsd een wsdl aan.
url: http://localhost:8080/ws/loanEligibility.wsdl

# testberichten

In directory http staan twee xml testberichten.
Deze berichten kunnen met tests.http worden gebruikt
In IntelliJ Ultimate kunnen de testen met de ingebouwde http client worden gestart met het groene pijltje.