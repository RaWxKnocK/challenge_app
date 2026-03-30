A Spring Boot REST API for managing monthly challenges. This app demonstrates CRUD operations (Create, Read, Update, Delete) using an in‑memory list, making it a simple but effective learning project for Spring Boot and RESTful services.

✨ Features
- REST API endpoints for managing challenges
- In‑memory storage (no database required)
- CRUD operations: add, view, update, delete
- Clean separation of controller, service, and model

📂 Project Structure
challenge_app/
 ├── src/main/java/com/learning/challengr_app/
 │   ├── ChallengrAppApplication.java   # Main entry point
 │   ├── Challenge.java                 # Model class
 │   ├── ChallengeService.java          # Business logic
 │   └── ChallengeController.java       # REST endpoints
 ├── pom.xml                            # Maven dependencies & build config
 ├── mvnw, mvnw.cmd                     # Maven wrapper scripts
 └── README.md                          # Documentation



⚙️ Prerequisites
- Java 21
- Maven 3.8+ (or use ./mvnw)
- IDE: IntelliJ IDEA / Eclipse / VS Code with Java extensions

▶️ Getting Started
Clone the Repository
git clone https://github.com/RaWxKnocK/challenge_app.git
cd challenge_app


Build the Project
./mvnw clean install


Run the Application
./mvnw spring-boot:run


The app will start at http://localhost:8080.

📌 API Endpoints
Get All Challenges
GET /challenges


Response:
[
  {
    "id": 1,
    "month": "January",
    "description": "Fitness challenge"
  }
]



Add a Challenge
POST /challenges


Request Body:
{
  "month": "February",
  "description": "Read 5 books"
}


Response:
Challenge added successfully



Get Challenge by Month
GET /challenges/{month}


Example:
GET /challenges/February



Update a Challenge
PUT /challenges/{id}


Request Body:
{
  "month": "March",
  "description": "30-day coding challenge"
}



Delete a Challenge
DELETE /challenges/{id}


Response:
Challenge deleted successfully



🛠️ Roadmap
- [ ] Add persistence with a database (MySQL/PostgreSQL)
- [ ] Implement validation and error handling
- [ ] Add unit and integration tests
- [ ] Secure endpoints with Spring Security
- [ ] Deploy to cloud (Heroku/AWS)

🤝 Contributing
- Fork the repo
- Create a feature branch (git checkout -b feature-name)
- Commit changes (git commit -m "Add feature")
- Push (git push origin feature-name)
- Open a Pull Request

📜 License
Licensed under the MIT License. You are free to use, modify, and distribute this project.
