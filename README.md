# FixMyCity - Civic Issue Reporting System

FixMyCity is a professional-grade civic issue management platform designed to help citizens report, track, and resolve city infrastructure problems. Built with Spring Boot (Java), PostgreSQL, and a modern HTML/CSS/JS frontend.

## Features

- Citizens can report issues (potholes, streetlights, etc.) with photos and location.
- Real-time tracking of issue status (pending, in-progress, resolved, closed).
- Admin portal for city officials to manage, assign, and resolve reports.
- Analytics dashboard for city management.
- Responsive, user-friendly web interface.

## Tech Stack

- **Backend:** Spring Boot, Spring Data JPA, Java 21
- **Database:** PostgreSQL
- **Frontend:** HTML, CSS, JavaScript (vanilla, Chart.js)
- **Build Tool:** Maven

## Project Structure

```
CivicIssueReportingSystem/
│
├── backend/
│   ├── src/main/java/com/civic/issuereporting/   # Spring Boot source code
│   ├── src/main/resources/application.properties # DB config
│   ├── pom.xml                                  # Maven dependencies
│   └── ...
│
├── frontend/
│   ├── index.html
│   ├── about-us.html
│   ├── login.html
│   ├── admin-login.html
│   ├── js/
│   │   ├── main.js
│   │   └── admin.js
│   ├── styles.css
│   └── ...
└── README.md
```

## Getting Started

### Prerequisites

- Java 21+
- Maven
- PostgreSQL

### Backend Setup

1. **Configure Database**

   Edit `backend/src/main/resources/application.properties`:

   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/fixmycity
   spring.datasource.username=your_db_user
   spring.datasource.password=your_db_password
   spring.jpa.hibernate.ddl-auto=update
   spring.jpa.show-sql=true
   spring.jpa.database-platform=org.hibernate.dialect.PostgreSQLDialect
   ```

2. **Run PostgreSQL**

   Create the database:
   ```sh
   createdb -U your_db_user fixmycity
   ```

3. **Build & Run Backend**

   ```sh
   cd backend
   ./mvnw spring-boot:run
   ```

   The backend will start at [http://localhost:8080](http://localhost:8080).

### Frontend Setup

1. Open `frontend/index.html` in your browser, or serve with a simple HTTP server:

   ```sh
   cd frontend
   # Python 3.x
   python -m http.server 8000
   # or use Live Server extension in VS Code
   ```

2. The frontend will connect to the backend API at `http://localhost:8080`.

## API Endpoints

- `GET /api/reports` — List all reports
- `POST /api/reports` — Submit a new report
- `PUT /api/reports/{id}` — Update report status
- `GET /api/reports/{id}` — Get report details
- ...and more (see backend controllers)

## Customization

- Update branding in `frontend/index.html` and other HTML files.
- Adjust database settings in `application.properties`.
- Extend backend logic in `backend/src/main/java/com/civic/issuereporting/controller/`.

## Contributing

Pull requests are welcome! Please open issues for suggestions or bugs.

## License

[Apache 2.0](LICENSE) (or specify your license)

---

*Empowering communities to report and resolve city issues.*
