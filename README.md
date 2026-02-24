Hi, I’m Manoj Kushwah 👋
👨‍💻 Java Backend Developer | Distributed Systems Enthusiast
I’m a Java Backend Developer based in India, currently pursuing my MCA. I specialize in building scalable, reliable backend systems using Java, Spring Boot, and microservices, with hands-on experience in event-driven architectures, REST API design, and distributed system fundamentals.
I enjoy working close to the system core — designing clean APIs, ensuring data consistency, handling asynchronous workflows, and building backend services that perform reliably under load. My interests strongly align with FinTech-style systems, real-time processing, and high-throughput architectures, including blockchain-adjacent backends.

🔭 Currently working on: Microservices, event-driven systems, and backend scalability
👯 Open to collaborate on: Java / Spring Boot / Distributed Systems projects
🤝 Open to roles: Java Backend Developer / Backend Engineer / Platform Engineer
📫 Reach me at: manojkushwah91115@gmail.com


🛠️ Tech Stack
Backend & Core

Java, Spring Boot
Microservices Architecture
REST APIs, Spring Data JPA, Spring Security (JWT)
Spring Cloud (Eureka, API Gateway, Config Server)

Messaging & Databases

Apache Kafka
PostgreSQL, MySQL, SQL

DevOps, Cloud & Tools

Docker, Linux
Git / GitHub, Maven
Jenkins (basic), Kubernetes (basic)
AWS (basic): EC2, S3, IAM, RDS, CloudWatch

Testing & Core Concepts

JUnit, Mockito
OOP, System Design, Distributed Systems Basics

Frontend (basic): JavaScript / React — used mainly for API integration, testing, and validating full-stack flows

🚀 Projects
💳 MicroPay – Digital Wallet & Payment Backend System
🔗 https://github.com/manojkushwah91/MicroPay
A backend-focused digital wallet and payment system built with Java and Spring Boot, using a microservices and event-driven architecture. It handles users, wallets, transactions, and payments, emphasizing data consistency, security, and scalability to simulate real-world fintech backend challenges.

Tech: Java 17, Spring Boot, Spring Data JPA, Spring Security, Spring Cloud (Eureka, API Gateway), Apache Kafka, PostgreSQL, JWT, Docker, Maven, Git
User & Wallet Management: User registration and authentication, automatic wallet creation on onboarding, secure access via JWT tokens.
Transaction & Payment Processing: Wallet-to-wallet fund transfers, asynchronous balance updates, transaction history tracking.
Event-Driven Architecture: Kafka used to publish transaction and wallet events, enabling loose coupling, improved responsiveness, and scalability.
Data Consistency: Spring transactional support for database operations, workflows designed to maintain consistency during partial failures, reliable balance updates.
Containerization: Backend services containerized with Docker for consistent local development and testing environments.
High-Level Transaction Flow: REST API request → Payment service validates and publishes event → Wallet service updates balances → Transaction status persisted → Response returned.
Design Focus: Backend-first microservices, clear separation of responsibilities, REST APIs for synchronous communication, Kafka for asynchronous processing, secure APIs with JWT, production-like Docker setup.
Capable of handling 500+ simulated transactions per second with low latency

🚖 RideShare – Ride Booking & Management Backend
🔗 https://github.com/manojkushwah91/rideshare
A backend-focused ride booking and management system built with Java and Spring Boot. It handles user and driver management, ride requests, driver assignment, trip lifecycle, and fare calculation, emphasizing clean REST APIs, asynchronous processing, and scalable backend design. The project simulates real-world backend challenges in ride-hailing platforms, with a basic frontend UI used only for API testing and flow validation.

Tech: Java, Spring Boot, REST APIs, Apache Kafka, MySQL, Docker, Git
User & Driver Management: User registration and profile handling; driver availability and assignment logic.
Ride Booking Flow: Create ride requests; assign drivers to rides; track ride status (requested, accepted, in-progress, completed); calculate fares based on trip details.
Asynchronous Event Processing: Publish and consume ride-related events via Apache Kafka; non-blocking processing for notifications and ride status updates; improved responsiveness and service decoupling.
Persistent Storage: Store users, rides, and trip history in MySQL; schema design supports trip lifecycle tracking.
Containerization: Containerize backend services with Docker for consistent local development and testing environments.

🛒 MicroMart – Cloud-Native E-Commerce Microservices Platform
🔗 https://github.com/manojkushwah91/MicroMart
A complete industry-grade microservices project that implements an e-commerce platform using a set of independent services, service discovery, API gateway, authentication, product catalog with caching, order processing, inventory management, payment handling, notifications, and full-stack Docker Compose deployment.

Tech: Java, Docker / Docker Compose, Spring Cloud (Eureka, API Gateway), JWT, Redis, Kafka, Resilience4j, Swagger, ELK stack
Eureka Server for service registration and discovery
API Gateway acting as the single entry point
Auth Service with JWT-ready security
Product Service with Redis caching support
Order Service (Kafka producer) for order creation
Inventory Service (Kafka consumer) for stock updates
Payment Service (Kafka consumer) with Resilience4j circuit breaker hooks
Notification Service (Kafka consumer) for alerts
Docker Compose file to spin up the entire stack
Swagger UI for API documentation
ELK stack for centralized logging and monitoring
Modular service layout ready for CI/CD pipelines

🗺️ CopMap Backend (Spring Boot)
🔗 https://github.com/manojkushwah91/copmap-backend
Backend service for a police operations screening task. It models patrolling and bandobast operations, officer assignment, live monitoring, alerts, and audit trails.

Tech: Spring Boot 3 / Java 17 (monolith), PostgreSQL (with JSONB for geo areas), Redis (caching, location snapshots, pub/sub), WebSockets (STOMP), JWT authentication, iText-based PDF reporting, Swagger/OpenAPI, Docker & Docker Compose
Operations: Create PATROL / BANDOBAST operations with GeoJSON area and time window; assign officers (availability check, no duplicates); close operations (immutable once closed) and evict from Redis.
Assignments: AssignmentService enforces rules; audit entries for create/assign/close.
Live Monitoring: LocationService persists locations, caches last location per officer/operation in Redis (TTL 5 min), broadcasts via WebSocket.
Alerts & Notifications: AlertService maps AlertDTO to entity; publishes to Redis alerts channel; NotificationService subscribes and logs mock email/FCM notifications.
Security: JWT-based auth with /auth/register and /auth/login; role-based method security on controllers.
Reporting & Audit: Generate PDF reports (assignments, recent locations, alerts, audit trail); Audit entity logs lifecycle.
WebSocket Flow: Officers send location DTO to /app/location; supervisors subscribe to /topic/monitor/{opId} for live updates.
API Endpoints: Auth (register, login), Operations (create, assign, close, report), Alerts (POST /alerts).
Testing: Service tests (Alert, Audit) with mocked repos/Redis; controller tests for HTTP mapping and status codes.
Future Split: Planned microservices (UserService, OperationService, MonitorService) with Kafka for live streams and audit replication.

🔗 Solana Transfer Extraction — Substreams
🔗 https://github.com/manojkushwah91/solana-transfer-extraction
Extract clean, structured transfer events from the Solana blockchain using Substreams. The package indexes SPL Token transfers, Token-2022 transfers, and native SOL transfers. It filters transactions by Program ID, parses instructions deterministically, and emits Protobuf-encoded transfer events suitable for analytics, wallets, dashboards, and sinks (SQL, Kafka, Parquet, etc.). Built from the sol-hello-world template and hardened for real-world Solana traffic.

Tech: Rust, Substreams (WASM-based indexing), Protobuf, Solana blockchain data
Program-ID–based transaction filtering (SPL Token, Token-2022, System Program)
Automatic exclusion of vote transactions (~80% of chain traffic)
Deterministic instruction parsing (no RPC calls)
Unified output for SPL + Token-2022 + native SOL transfers
Protobuf-first design (JSON supported for testing)
GUI-friendly for rapid iteration
Registry-publishable Substreams package
Modules: map_filtered_transactions and map_my_data
Custom Protobuf schema (TokenTransfer) with fields: tx_signature, slot, block_time, from, to, amount, mint, token_program, is_native_sol
Quick start with substreams build, substreams auth, substreams gui
CLI example for filtering and outputting JSON
Imports: solana_common, spl_token from streamingfast
Next steps include expanding instruction coverage, multi-sink examples, and validation against high-volume tokens.

📦 Inventory Management System
🔗 https://github.com/manojkushwah91/inventory
A simple Spring Boot based Inventory Management System designed for a small retail store. The application provides REST APIs to manage products and their quantities.

Tech: Java, Spring Boot, Spring Web, Spring Data JPA, H2 In-Memory Database, Maven
Add products to the inventory
Update product quantities
Remove products from the inventory
View all products in the inventory

🎥 Movie Management REST API
🔗 https://github.com/manojkushwah91/movieapi
A simple and professional Java Spring Boot RESTful backend application for managing a collection of movies. Developed strictly according to the given sample task, using in-memory data storage (ArrayList) and clean REST API design.

Tech: Java 17, Spring Boot, Spring Web, Jakarta Validation, Maven, Docker, Render (Hosting)
RESTful API Design
In-Memory Data Storage using ArrayList
Input Validation using jakarta.validation
Clean Layered Architecture
No Database Used (as required)
Production-ready structure for demo


🎓 Education & Experience

Master of Computer Applications (MCA) — Bansal Institute of Science and Technology
Bachelor of Computer Applications (BCA) — Devi Ahilya University
Software Engineering Job Simulation (Virtual)JPMorgan Chase & Co.
Worked on Spring Boot REST APIs, Kafka integration, and in-memory databases
Focused on backend workflows, messaging, and testing



  
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&#x26;logo=linkedin&#x26;logoColor=white">
  
11.7sgive me this in a editor or md file so i can paste directly there give me fully complete dont miss anythingHi, I’m Manoj Kushwah 👋
👨‍💻 Java Backend Developer | Distributed Systems Enthusiast
I’m a Java Backend Developer based in India, currently pursuing my MCA. I specialize in building scalable, reliable backend systems using Java, Spring Boot, and microservices, with hands-on experience in event-driven architectures, REST API design, and distributed system fundamentals.
I enjoy working close to the system core — designing clean APIs, ensuring data consistency, handling asynchronous workflows, and building backend services that perform reliably under load. My interests strongly align with FinTech-style systems, real-time processing, and high-throughput architectures, including blockchain-adjacent backends.

🔭 Currently working on: Microservices, event-driven systems, and backend scalability
👯 Open to collaborate on: Java / Spring Boot / Distributed Systems projects
🤝 Open to roles: Java Backend Developer / Backend Engineer / Platform Engineer
📫 Reach me at: manojkushwah91115@gmail.com


🛠️ Tech Stack
Backend & Core

Java, Spring Boot
Microservices Architecture
REST APIs, Spring Data JPA, Spring Security (JWT)
Spring Cloud (Eureka, API Gateway, Config Server)

Messaging & Databases

Apache Kafka
PostgreSQL, MySQL, SQL

DevOps, Cloud & Tools

Docker, Linux
Git / GitHub, Maven
Jenkins (basic), Kubernetes (basic)
AWS (basic): EC2, S3, IAM, RDS, CloudWatch

Testing & Core Concepts

JUnit, Mockito
OOP, System Design, Distributed Systems Basics

Frontend (basic): JavaScript / React — used mainly for API integration, testing, and validating full-stack flows

🚀 Projects
💳 MicroPay – Digital Wallet & Payment Backend System
🔗 https://github.com/manojkushwah91/MicroPay
A backend-focused digital wallet and payment system built with Java and Spring Boot, using a microservices and event-driven architecture. It handles users, wallets, transactions, and payments, emphasizing data consistency, security, and scalability to simulate real-world fintech backend challenges.

Tech: Java 17, Spring Boot, Spring Data JPA, Spring Security, Spring Cloud (Eureka, API Gateway), Apache Kafka, PostgreSQL, JWT, Docker, Maven, Git
User & Wallet Management: User registration and authentication, automatic wallet creation on onboarding, secure access via JWT tokens.
Transaction & Payment Processing: Wallet-to-wallet fund transfers, asynchronous balance updates, transaction history tracking.
Event-Driven Architecture: Kafka used to publish transaction and wallet events, enabling loose coupling, improved responsiveness, and scalability.
Data Consistency: Spring transactional support for database operations, workflows designed to maintain consistency during partial failures, reliable balance updates.
Containerization: Backend services containerized with Docker for consistent local development and testing environments.
High-Level Transaction Flow: REST API request → Payment service validates and publishes event → Wallet service updates balances → Transaction status persisted → Response returned.
Design Focus: Backend-first microservices, clear separation of responsibilities, REST APIs for synchronous communication, Kafka for asynchronous processing, secure APIs with JWT, production-like Docker setup.
Capable of handling 500+ simulated transactions per second with low latency

🚖 RideShare – Ride Booking & Management Backend
🔗 https://github.com/manojkushwah91/rideshare
A backend-focused ride booking and management system built with Java and Spring Boot. It handles user and driver management, ride requests, driver assignment, trip lifecycle, and fare calculation, emphasizing clean REST APIs, asynchronous processing, and scalable backend design. The project simulates real-world backend challenges in ride-hailing platforms, with a basic frontend UI used only for API testing and flow validation.

Tech: Java, Spring Boot, REST APIs, Apache Kafka, MySQL, Docker, Git
User & Driver Management: User registration and profile handling; driver availability and assignment logic.
Ride Booking Flow: Create ride requests; assign drivers to rides; track ride status (requested, accepted, in-progress, completed); calculate fares based on trip details.
Asynchronous Event Processing: Publish and consume ride-related events via Apache Kafka; non-blocking processing for notifications and ride status updates; improved responsiveness and service decoupling.
Persistent Storage: Store users, rides, and trip history in MySQL; schema design supports trip lifecycle tracking.
Containerization: Containerize backend services with Docker for consistent local development and testing environments.

🛒 MicroMart – Cloud-Native E-Commerce Microservices Platform
🔗 https://github.com/manojkushwah91/MicroMart
A complete industry-grade microservices project that implements an e-commerce platform using a set of independent services, service discovery, API gateway, authentication, product catalog with caching, order processing, inventory management, payment handling, notifications, and full-stack Docker Compose deployment.

Tech: Java, Docker / Docker Compose, Spring Cloud (Eureka, API Gateway), JWT, Redis, Kafka, Resilience4j, Swagger, ELK stack
Eureka Server for service registration and discovery
API Gateway acting as the single entry point
Auth Service with JWT-ready security
Product Service with Redis caching support
Order Service (Kafka producer) for order creation
Inventory Service (Kafka consumer) for stock updates
Payment Service (Kafka consumer) with Resilience4j circuit breaker hooks
Notification Service (Kafka consumer) for alerts
Docker Compose file to spin up the entire stack
Swagger UI for API documentation
ELK stack for centralized logging and monitoring
Modular service layout ready for CI/CD pipelines

🗺️ CopMap Backend (Spring Boot)
🔗 https://github.com/manojkushwah91/copmap-backend
Backend service for a police operations screening task. It models patrolling and bandobast operations, officer assignment, live monitoring, alerts, and audit trails.

Tech: Spring Boot 3 / Java 17 (monolith), PostgreSQL (with JSONB for geo areas), Redis (caching, location snapshots, pub/sub), WebSockets (STOMP), JWT authentication, iText-based PDF reporting, Swagger/OpenAPI, Docker & Docker Compose
Operations: Create PATROL / BANDOBAST operations with GeoJSON area and time window; assign officers (availability check, no duplicates); close operations (immutable once closed) and evict from Redis.
Assignments: AssignmentService enforces rules; audit entries for create/assign/close.
Live Monitoring: LocationService persists locations, caches last location per officer/operation in Redis (TTL 5 min), broadcasts via WebSocket.
Alerts & Notifications: AlertService maps AlertDTO to entity; publishes to Redis alerts channel; NotificationService subscribes and logs mock email/FCM notifications.
Security: JWT-based auth with /auth/register and /auth/login; role-based method security on controllers.
Reporting & Audit: Generate PDF reports (assignments, recent locations, alerts, audit trail); Audit entity logs lifecycle.
WebSocket Flow: Officers send location DTO to /app/location; supervisors subscribe to /topic/monitor/{opId} for live updates.
API Endpoints: Auth (register, login), Operations (create, assign, close, report), Alerts (POST /alerts).
Testing: Service tests (Alert, Audit) with mocked repos/Redis; controller tests for HTTP mapping and status codes.
Future Split: Planned microservices (UserService, OperationService, MonitorService) with Kafka for live streams and audit replication.

🔗 Solana Transfer Extraction — Substreams
🔗 https://github.com/manojkushwah91/solana-transfer-extraction
Extract clean, structured transfer events from the Solana blockchain using Substreams. The package indexes SPL Token transfers, Token-2022 transfers, and native SOL transfers. It filters transactions by Program ID, parses instructions deterministically, and emits Protobuf-encoded transfer events suitable for analytics, wallets, dashboards, and sinks (SQL, Kafka, Parquet, etc.). Built from the sol-hello-world template and hardened for real-world Solana traffic.

Tech: Rust, Substreams (WASM-based indexing), Protobuf, Solana blockchain data
Program-ID–based transaction filtering (SPL Token, Token-2022, System Program)
Automatic exclusion of vote transactions (~80% of chain traffic)
Deterministic instruction parsing (no RPC calls)
Unified output for SPL + Token-2022 + native SOL transfers
Protobuf-first design (JSON supported for testing)
GUI-friendly for rapid iteration
Registry-publishable Substreams package
Modules: map_filtered_transactions and map_my_data
Custom Protobuf schema (TokenTransfer) with fields: tx_signature, slot, block_time, from, to, amount, mint, token_program, is_native_sol
Quick start with substreams build, substreams auth, substreams gui
CLI example for filtering and outputting JSON
Imports: solana_common, spl_token from streamingfast
Next steps include expanding instruction coverage, multi-sink examples, and validation against high-volume tokens.

📦 Inventory Management System
🔗 https://github.com/manojkushwah91/inventory
A simple Spring Boot based Inventory Management System designed for a small retail store. The application provides REST APIs to manage products and their quantities.

Tech: Java, Spring Boot, Spring Web, Spring Data JPA, H2 In-Memory Database, Maven
Add products to the inventory
Update product quantities
Remove products from the inventory
View all products in the inventory

🎥 Movie Management REST API
🔗 https://github.com/manojkushwah91/movieapi
A simple and professional Java Spring Boot RESTful backend application for managing a collection of movies. Developed strictly according to the given sample task, using in-memory data storage (ArrayList) and clean REST API design.

Tech: Java 17, Spring Boot, Spring Web, Jakarta Validation, Maven, Docker, Render (Hosting)
RESTful API Design
In-Memory Data Storage using ArrayList
Input Validation using jakarta.validation
Clean Layered Architecture
No Database Used (as required)
Production-ready structure for demo


🎓 Education & Experience

Master of Computer Applications (MCA) — Bansal Institute of Science and Technology
Bachelor of Computer Applications (BCA) — Devi Ahilya University
Software Engineering Job Simulation (Virtual)JPMorgan Chase & Co.
Worked on Spring Boot REST APIs, Kafka integration, and in-memory databases
Focused on backend workflows, messaging, and testing



  
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&#x26;logo=linkedin&#x26;logoColor=white">
