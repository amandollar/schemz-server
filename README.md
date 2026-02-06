# Schemz — Server

Small Spring Boot server for Schemz. Provides REST endpoints for authentication, scheme management, and an eligibility engine.

Prerequisites
- Java 17
- Apache Maven

Build
Run from the repository root:

```bash
mvn -f server clean package
```

Run
- Run with Maven:

```bash
mvn -f server spring-boot:run
```

- Or run the built jar:

```bash
java -jar server/target/server-0.0.1-SNAPSHOT.jar
```

Tests

```bash
mvn -f server test
```

Important files
- `server/pom.xml` — Maven project and dependencies (Spring Boot 3.2, Java 17)
- `server/src/main/resources/application.properties` — runtime configuration (H2 in-memory DB, server port 8080)
- `server/src/main/java/com/schemz/server` — application sources
- `plan.txt` — project plan

Configuration
- The app uses an H2 in-memory database by default. Key properties are in `server/src/main/resources/application.properties`.
- If you provide external DB or JWT secrets, set environment variables or override properties before running.

Project structure (high level)
- `server/` — Spring Boot service (source, tests, pom)

Notes
- A `.gitignore` file was added to ignore `target/`, IDE files, and common artifacts.

License
- See project owner for licensing. Feel free to add a `LICENSE` file.
