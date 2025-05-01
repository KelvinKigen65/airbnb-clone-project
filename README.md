# Airbnb Clone Project

## Project Overview

This project is a simplified clone of the Airbnb platform, aimed at providing users with the ability to list, search, and book rentals. The objective is to practice backend development, team collaboration, ,Problem Solving and software development application.

### Project Goals

- Build a scalable backend with API applications for managing users, properties, bookings, and payments.
- Ensure secure and reliable data handling through robust authentication and authorization mechanisms.
- Ensuring data integrity and data privacy through authentications.



## Team Roles

### Backend Developer
Responsible for implementing the core logic of the application, including API applications, authentication, and interaction with the database.

### Frontend Developer
Designs and implements the user interface, ensuring a responsive and intuitive user experience.

### Database Administrator (DBA)
Designs and manages the database schema, optimizes queries, and ensures data integrity.

### DevOps Engineer
Handles deployment, CI/CD pipeline integration, and infrastructure management to ensure smooth delivery of features.

### QA Engineer
Tests the application for bugs, usability, and performance issues and ensures that new features meet requirements.



## Technology Stack

### Django
A high-level Python web framework used to build robust RESTful APIs and manage backend logic.

### PostgreSQL
An open-source relational database used for storing structured data such as users, properties, and bookings.

### GraphQL
An API query language used to fetch the data needed by the frontend, improving performance and flexibility.

### Docker
Used to containerize the application for deployment and development environments.

### GitHub Actions
A CI/CD tool used to automate testing and deployment workflows directly from the GitHub repository.


## Database Design

### Users
- `id` (UUID)
- `name`
- `email`
- `password_hash`
- `is_host` (Boolean)

### Properties
- `id`
- `title`
- `description`
- `location`
- `owner_id` (ForeignKey to Users)

### Bookings
- `id`
- `user_id` (ForeignKey to Users)
- `property_id` (ForeignKey to Properties)
- `start_date`
- `end_date`

### Reviews
- `id`
- `booking_id` (ForeignKey to Bookings)
- `rating`
- `comment`
- `created_at`

### Payments
- `id`
- `booking_id` (ForeignKey to Bookings)
- `amount`
- `status`
- `payment_date`

**Entity Relationships:**
- A user can own multiple properties.
- A property can have multiple bookings.
- A booking is associated with one property and one user.
- Each booking can have one review.
- Each booking corresponds to a payment.

---

## Feature Breakdown

### User Management
Allows users to register, log in, and manage their profiles. Hosts can list properties; guests can make bookings.

### Property Management
Users can add, edit, and delete property listings with descriptions, pricing, and availability.

### Booking System
Guests can search for properties and book available ones for specific dates.

### Review System
Guests can leave feedback and ratings for properties they’ve stayed in.

### Payment Integration
Handles secure payment processing for bookings and stores payment status.



## API Security

### Authentication
Uses token-based authentication to verify user identities.

### Authorization
Ensures users can only access or modify resources they own.


**Importance:**
- Authentication ensures only registered users access the platform.
- Authorization protects data integrity and ensure user privacy.

## CI/CD Pipeline

Continuous Integration (CI) and Continuous Deployment (CD) help maintain code quality and facilitates project development.

### Importance
- Automates testing and reduces bugs.
- Saves developer time through automation.

### Tools
- **GitHub Actions**: For automating tests and deployments.
- **Docker**: To ensure consistency across development, testing, and production environments.
- **AWS / DigitalOcean**: Used for deployment.


