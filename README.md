# Medical microservices configuration

This coursework contains:

- `config-service`: Spring Cloud Config Server, running on port `8888`.
- `patient-service`: Spring Boot service that loads its configuration from Config Server.
- `medical-config-repo`: Git repository containing centralized service configuration.

Start the Config Service:

```bash
cd config-service
mvn spring-boot:run
```

Then verify the profiles at:

- `http://localhost:8888/patient-service/dev`
- `http://localhost:8888/patient-service/prod`

Start the Patient Service in a second terminal:

```bash
cd patient-service
mvn spring-boot:run -Dspring-boot.run.profiles=dev
```

Use `-Dspring-boot.run.profiles=prod` to run with PostgreSQL on port `8082`.
# micro_btvn07_01
