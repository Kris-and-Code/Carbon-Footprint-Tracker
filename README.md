# Carbon Footprint Tracker and Offset Platform

A comprehensive web application to help users track their carbon emissions, get personalized reduction recommendations, and purchase carbon offsets to achieve carbon neutrality.

## 🌱 Project Overview

This application addresses the critical need for climate action by providing individuals and organizations with tools to:
- **Track** daily carbon emissions from various activities
- **Analyze** emission patterns and trends
- **Get recommendations** for reducing carbon footprint
- **Purchase carbon offsets** to neutralize remaining emissions
- **Visualize** progress through interactive charts and dashboards

## 🚀 Tech Stack

### Backend
- **Java 21** - Latest LTS version with modern features
- **Spring Boot 3.2.5** - Rapid application development framework
- **Spring Data JPA** - Data persistence and ORM
- **Spring Security** - Authentication and authorization
- **PostgreSQL** - Robust relational database
- **JJWT** - JSON Web Token implementation for secure authentication

### Frontend
- **Thymeleaf** - Server-side templating engine
- **Chart.js** - Interactive data visualizations
- **Bootstrap** - Responsive UI framework
- **JavaScript** - Dynamic client-side functionality

### Tools & Infrastructure
- **Maven** - Dependency management and build tool
- **Docker** - Containerization for consistent deployment
- **JUnit** - Unit and integration testing
- **Swagger/OpenAPI** - API documentation
- **Git** - Version control
- **Heroku/AWS** - Cloud deployment options

## 📋 Prerequisites

Before running this application, ensure you have the following installed:

- **Java Development Kit (JDK) 21**
- **Maven 3.6+**
- **Docker Desktop** (for database)
- **Git**

## 🛠️ Installation & Setup

### 1. Clone the Repository
```bash
git clone git@github.com:Kris-and-Code/Carbon-Footprint-Tracker.git
cd carbon-footprint-tracker
```

### 2. Start PostgreSQL Database
```bash
docker compose up -d
```

This will start a PostgreSQL database with the following configuration:
- **Host**: localhost:5432
- **Database**: carbon_tracker_db
- **Username**: admin
- **Password**: password

### 3. Build and Run the Application
```bash
# Build the project
mvn clean install

# Run the application
mvn spring-boot:run
```

The application will be available at: `http://localhost:8080`

### 4. Access the Application
- **Main Application**: http://localhost:8080
- **API Documentation**: http://localhost:8080/swagger-ui.html
- **Database**: localhost:5432 (via Docker)

## 🏗️ Project Structure

```
carbon-footprint-tracker/
├── src/
│   ├── main/
│   │   ├── java/com/carbontracker/
│   │   │   ├── config/           # Configuration classes
│   │   │   ├── controller/       # REST controllers
│   │   │   ├── model/           # Entity classes
│   │   │   ├── repository/      # Data access layer
│   │   │   ├── service/         # Business logic
│   │   │   ├── security/        # Security configuration
│   │   │   └── util/            # Utility classes
│   │   └── resources/
│   │       ├── static/          # CSS, JS, images
│   │       ├── templates/       # Thymeleaf templates
│   │       └── application.properties
│   └── test/                    # Test classes
├── docker-compose.yml           # Database configuration
├── pom.xml                      # Maven dependencies
└── README.md                    # This file
```

## 🎯 Core Features

### 1. User Management
- User registration and authentication
- Profile management
- Role-based access control

### 2. Carbon Footprint Tracking
- Log daily activities (transportation, energy, food, etc.)
- Automatic carbon emission calculations
- Historical data tracking
- Category-wise emission breakdown

### 3. Analytics & Visualization
- Interactive charts and graphs
- Emission trends over time
- Comparison with averages
- Progress tracking towards goals

### 4. Recommendations Engine
- Personalized reduction suggestions
- Actionable tips based on usage patterns
- Impact assessment for different actions

### 5. Carbon Offset Marketplace
- Browse verified carbon offset projects
- Purchase offsets to neutralize emissions
- Track offset portfolio
- Certification and verification

### 6. Reporting
- Monthly/quarterly emission reports
- Carbon neutrality certificates
- Export functionality
- Social sharing capabilities

## 🔧 Configuration

### Database Configuration
The application uses PostgreSQL. Key configuration in `application.properties`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/carbon_tracker_db
spring.datasource.username=admin
spring.datasource.password=password
spring.jpa.hibernate.ddl-auto=update
```

### Environment Variables
For production deployment, consider using environment variables:

```bash
export DB_URL=your_production_db_url
export DB_USERNAME=your_db_username
export DB_PASSWORD=your_db_password
export JWT_SECRET=your_jwt_secret
```

## 🧪 Testing

Run the test suite:

```bash
# Run all tests
mvn test

# Run tests with coverage
mvn test jacoco:report

# Run integration tests
mvn verify
```

## 🚀 Deployment

### Local Development
```bash
mvn spring-boot:run
```

### Docker Deployment
```bash
# Build Docker image
docker build -t carbon-tracker .

# Run container
docker run -p 8080:8080 carbon-tracker
```

### Cloud Deployment

#### Heroku
```bash
# Create Heroku app
heroku create your-app-name

# Add PostgreSQL addon
heroku addons:create heroku-postgresql:hobby-dev

# Deploy
git push heroku main
```

#### AWS
- Use AWS Elastic Beanstalk
- Configure RDS for PostgreSQL
- Set up environment variables
- Deploy using AWS CLI or console

## 📊 API Documentation

Once the application is running, access the interactive API documentation at:
- **Swagger UI**: http://localhost:8080/swagger-ui.html
- **OpenAPI JSON**: http://localhost:8080/v3/api-docs

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow Java coding conventions
- Write unit tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting PR

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Carbon emission calculation methodologies
- Open-source libraries and frameworks
- Climate science research and data
- Carbon offset verification standards

## 📞 Support

For support and questions:
- Create an issue in the repository
- Contact the development team
- Check the documentation

## 🔮 Future Enhancements

- Mobile application (React Native/Flutter)
- Machine learning for better recommendations
- Integration with IoT devices
- Blockchain-based carbon credit tracking
- Social features and community challenges
- Advanced analytics and AI insights

---

**Made with ❤️ for a sustainable future** 