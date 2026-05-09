# Digital Complaint Escalation & Management System

**Resolutix** — An intelligent, lightning-fast complaint escalation and resolution platform built on a dual-stack architecture.

![Node.js](https://img.shields.io/badge/Node.js-18.x-green?style=flat-square&logo=nodejs)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen?style=flat-square&logo=springboot)
![MongoDB](https://img.shields.io/badge/MongoDB-7.x-green?style=flat-square&logo=mongodb)
![Java](https://img.shields.io/badge/Java-17-orange?style=flat-square&logo=java)

Made by [Riya]

---

## 📋 Overview

Resolutix is a comprehensive complaint management system that streamlines the process of reporting, tracking, and resolving complaints. Features include:

- 🎨 **Animated Landing Page** - Beautiful hero section with gradient title and smooth scroll effects
- 📊 **Live Platform Stats** - Real-time metrics for total complaints, resolved, pending, and success rates
- ✨ **Feature Cards** - Glassmorphism design with smooth interactions
- 🔐 **Authentication** - Session-based login with Passport.js and bcrypt password hashing
- 👥 **Role-Based Access** - User, Junior Engineer, and Admin roles with different dashboards
- 📱 **Responsive Dashboard** - Track personal performance metrics and complaint history
- ⚡ **Fast API** - RESTful backend built with Java Spring Boot

---

## 🏗️ Architecture

### Frontend
- **Node.js + Express** - Web server and route handling
- **Handlebars** - Template engine for dynamic views
- **Bootstrap** - Responsive UI framework
- **Chart.js** - Data visualization for statistics

### Backend
- **Java Spring Boot** - RESTful API server
- **Spring Security** - Authentication and authorization
- **Spring Data JPA** - Database ORM

### Database
- **MongoDB** - NoSQL data storage for scalability

---

## 📁 Project Structure

```
complaint-system/
├── app.js                    # Express app entry point
├── db.js                     # MongoDB connection
├── routes/
│   └── index.js             # All route handlers
├── models/
│   ├── user.js              # User schema
│   ├── complaint.js         # Complaint schema
│   ├── complaint-mapping.js # Complaint assignment schema
│   └── feedback.js          # Feedback schema
├── views/
│   ├── landing.handlebars   # Animated landing page
│   ├── index.handlebars     # User dashboard
│   ├── admin/               # Admin views
│   ├── junior/              # Junior Engineer views
│   └── layouts/main.handlebars  # Shared layout
├── public/
│   ├── css/style.css        # Custom styles
│   └── images/              # Assets
└── spring-backend/          # Java Spring Boot API
    ├── src/main/java/com/example/demo/
    │   ├── controllers/     # REST endpoints
    │   ├── models/          # Entity classes
    │   ├── repositories/    # Data access layer
    │   └── security/        # Security config
    └── pom.xml              # Maven dependencies
```

---

## ✨ Key Features

### User Dashboard
- View assigned complaints
- Mark complaints as resolved
- Track personal performance metrics
- File new complaints with forms

### Junior Engineer Dashboard
- View assigned complaints
- Update complaint status
- Submit feedback and notes
- Performance analytics

### Admin Dashboard
- View all complaints and users
- Assign complaints to engineers
- Monitor system-wide statistics
- Manage user feedback submissions

### Authentication
- User registration with validation
- Secure login with bcrypt hashing
- Session management
- Seamless redirect flows

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18.x
- Java 17+
- MongoDB 7.x
- Maven 3.8+

### Frontend Setup

```bash
npm install
npm start
```

Visit `http://localhost:3000`

### Backend Setup

```bash
cd spring-backend
mvn clean install
mvn spring-boot:run
```

API runs on `http://localhost:8080`

---

## 🔧 Configuration

### MongoDB Connection
Edit `db.js`:
```javascript
const mongoURI = 'mongodb://localhost:27017/complaint-system';
```

### Spring Boot Properties
Edit `spring-backend/src/main/resources/application.properties`:
```properties
spring.data.mongodb.uri=mongodb://localhost:27017/complaint-system
```

---

## 📊 Database Schema

### Users
- userId, name, email, password, role

### Complaints
- complaintId, title, description, status, createdDate

### Complaint Mapping
- mappingId, complaintId, assignedTo, status

### Feedback
- feedbackId, complaintId, feedback, rating

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

---

## 📄 License

MIT License - See LICENSE file for details

---

## 👨‍💼 Authors

- **Riya** - Full Stack Developer

---

## 📞 Support

For issues and questions, please open an issue on GitHub or contact the development team.

---

**Built with ❤️ for efficient complaint management**
