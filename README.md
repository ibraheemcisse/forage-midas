# Midas Core — JPMC Software Engineering Virtual Experience

A financial transaction processing microservice built as part of the **JPMorgan Chase Software Engineering Virtual Experience** on Forage.

Midas Core is responsible for receiving, validating, and recording financial transactions at scale using Apache Kafka, Spring Boot, and JPA.

---

## Architecture
```
[Frontend / Test Producer]
          ↓
  [Kafka Topic: trader-updates]
          ↓
  [TransactionListener]
          ↓
  [Validation Layer]
          ↓
  [SQL Database (H2)]
          ↓
  [REST API]
```

---

## Tech Stack

| Technology | Purpose |
|------------|---------|
| Java 17 | Core language |
| Spring Boot 3.2.5 | Application framework |
| Apache Kafka 3.1.4 | Message queue / event streaming |
| Spring Data JPA | Database persistence |
| H2 Database | In-memory SQL database |
| Maven | Build tool |
| Testcontainers | Embedded Kafka for testing |

---

## Tasks

### ✅ Task 1 — Environment Setup
- Configured Java 17, Maven, Spring Boot
- Added required dependencies to pom.xml
- Fixed maven-compiler-plugin version mismatch (3.11.0 → 3.13.0)

### ✅ Task 2 — Kafka Integration
- Created TransactionListener to consume messages from trader-updates topic
- Configured Kafka JSON serializer/deserializer for Transaction domain objects
- Verified message flow using embedded Kafka and TaskTwoTests

### 🔄 Task 3 — Persistence (In Progress)

### ⬜ Task 4 — Validation

### ⬜ Task 5 — REST API

---

## Getting Started

### Prerequisites
- Java 17
- Maven 3.8+

### Clone
git clone https://github.com/ibraheemcisse/forage-midas.git
cd forage-midas

### Build
mvn clean install

### Run
mvn spring-boot:run

### Test
mvn test
mvn test -Dtest=TaskTwoTests

---


