Complete Spring Boot Online Voting System

How to run:
1. Install Java 17+ and Maven.
2. Start MySQL and create/import database:
   - Run the included schema.sql to create tables (database: voting_system).
3. Update DB credentials in src/main/resources/application.properties if needed.
4. Build and run:
   mvn clean install
   mvn spring-boot:run
5. Open http://localhost:8080/

Flow:
- Home: /index -> Admin Login, Voter Login, Voter Registration
- Admin Login: /admin/login -> Admin Dashboard (/admin/dashboard)
  - Add candidate, Remove candidate, Remove voter, View results
- Voter Register: /voter/register
- Voter Login: /voter/login -> Voter Dashboard (/voter/dashboard) -> Vote once

Default: No admin created. Create admin via SQL:
INSERT INTO admin (username, password) VALUES ('admin','admin123');
Note: Passwords stored in plain text for demo. For production, use hashing and Spring Security.
