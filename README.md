# Spring Boot JWT Authentication

## Overview
A robust implementation of JSON Web Token (JWT) authentication within a Spring Boot application. This project provides a secure framework for handling user authentication and authorization, with a focus on stateless security architecture.

## Features
- **JWT Authentication**: Secure token-based authentication system
- **Stateless Architecture**: No server-side session storage required
- **Token Validation**: Comprehensive token validation and verification
- **Spring Security Integration**: Leverages Spring Security's authentication mechanisms
- **RESTful API**: Clean API endpoint for authentication
- **Exception Handling**: Proper error responses for authentication failures

## Technical Stack
- Java 24
- Spring Boot 3.5.0
- Spring Security
- JJWT (Java JWT Library)
- Maven

## Getting Started

### Prerequisites
- JDK 24+
- Maven 3.6+

### Installation
1. Clone the repository
   ```
   git clone https://github.com/PunMahesh/spring-boot-jwt-auth.git
   ```
2. Navigate to the project directory
   ```
   cd spring-boot-jwt-auth
   ```
3. Build the project
   ```
   mvn clean install
   ```
4. Run the application
   ```
   mvn spring-boot:run
   ```

## API Usage

### Authentication
**Endpoint**: `POST /authenticate`

**Request Body**:
```json
{
  "username": "user",
  "password": "password"
}
```

**Successful Response** (200 OK):
```json
{
  "token": "eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1c2VyIiwiaWF0IjoxNjQ..."
}
```

## Security Considerations
- The JWT secret key is generated at runtime
- Token expiration is set to 5 hours by default
- All endpoints except `/authenticate` require authentication
- CSRF protection is disabled for stateless operation
- Password storage uses BCrypt hashing

## Project Structure
```
com.auth.sbbank/
├── config/              # Security configurations
├── controller/          # REST controllers
├── model/               # Data models
└── util/                # Utility classes
```

## Future Enhancements
- Database integration for user management
- Refresh token implementation
- Role-based authorization
- Token blacklisting

## Contact
For questions or support, please open an issue in the GitHub repository.