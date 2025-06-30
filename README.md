# AirBnB Clone Project

This project is a backend clone of the AirBnB platform. It's designed to help us understand how full-stack applications work, from database design to API development.

#  📌 Project Goals

- Build a robust backend for an AirBnB-like platform.
- Practice user authentication, property listings, booking flow, and payment integration.
- Learn to work in a team using Git, GitHub, and Agile methodologies.

# 🛠️ Tech Stack

- **Language**: Python
- **Framework**: Flask (or Django depending on final decision)
- **Database**: MySQL
- **Tools**: Git, GitHub, Draw.io, Postman
# Roles and Responsibilities - AirBnB Clone Project

# Team Roles

## 1. Backend Developer
- Build and maintain the server-side logic of the application.
- Develop RESTful APIs for user registration, login, property management, and bookings.
- Ensure secure authentication and authorization flows.
- Write unit and integration tests for backend functionality.

## 2. Database Administrator (DBA)
- Design and maintain the project's database schema.
- Ensure data integrity, consistency, and security.
- Write and optimize SQL queries and stored procedures.
- Manage backups and monitor performance.

## 3. DevOps Engineer
- Set up version control workflows and CI/CD pipelines.
- Configure development and production environments.
- Handle deployment, monitoring, and scaling of the application.
- Ensure system reliability and uptime.

## 4. Frontend Developer 
- Build user-facing components and integrate them with backend APIs.
- Ensure responsive and accessible UI design.
- Work closely with the backend team to handle API consumption.
- Handle state management and user interactions.

## 5. Project Manager / Scrum Master
- Organize team meetings and manage the development workflow.
- Define project goals, timelines, and deliverables.
- Monitor progress and remove blockers.
- Facilitate communication between team members.

## 6. QA Tester
- Test features for bugs and usability issues.
- Create test cases and scenarios based on project requirements.
- Perform manual and automated testing.
- Report bugs and verify fixes.
- 
## 🧰 Technology Stack
- **Django**: A high-level Python web framework used to build the backend logic and RESTful APIs quickly and securely.
- **PostgreSQL**: A powerful open-source relational database used to store and manage user, property, booking, and payment data.
- **GraphQL**: A query language and runtime that allows clients to request exactly the data they need, improving efficiency over traditional REST endpoints.
- **Docker**: Used to containerize the application, ensuring consistent environments for development, testing, and deployment.
- **Git & GitHub**: For version control and team collaboration. Git tracks changes in code, and GitHub hosts the project repository.
- **Draw.io**: A diagramming tool used to design system architecture, use case diagrams, and ER models.
- **Postman**: A tool for testing and debugging API endpoints during development.
- **Python**: The core programming language used to write server logic and handle data processing.

# 🗄️ Database Design

This section outlines the main entities in the AirBnB Clone project and how they relate to each other.

## 📌 Entities and Key Fields

### 1. Users
- `id`: Unique identifier
- `name`: Full name of the user
- `email`: Email address (used for login)
- `password_hash`: Hashed password for authentication
- `role`: Defines if the user is a host or guest

### 2. Properties
- `id`: Unique identifier
- `user_id`: Owner of the property (foreign key to Users)
- `title`: Short name of the listing
- `location`: Address or general area
- `price_per_night`: Cost to book per night

### 3. Bookings
- `id`: Unique identifier
- `user_id`: The guest making the booking (foreign key to Users)
- `property_id`: The property being booked (foreign key to Properties)
- `start_date`: Start of the booking
- `end_date`: End of the booking

### 4. Reviews
- `id`: Unique identifier
- `user_id`: The user writing the review (foreign key to Users)
- `property_id`: The property being reviewed
- `rating`: Numeric score (e.g., 1 to 5)
- `comment`: Text feedback

### 5. Payments
- `id`: Unique identifier
- `booking_id`: Related booking (foreign key to Bookings)
- `amount`: Payment amount
- `payment_status`: Status (e.g., pending, completed)
- `payment_date`: When the payment was made

### 🔗 Entity Relationships

- A **User** can create multiple **Properties** (host role).
- A **User** can make multiple **Bookings** (guest role).
- A **Property** can have many **Bookings** and **Reviews**.
- A **Booking** is made by one **User** and belongs to one **Property**.
- A **Payment** is linked to one **Booking**.
- A **Review** is written by a **User** for a **Property** they’ve booked.

# 🧩 Feature Breakdown

This section outlines the core features included in the AirBnB Clone project and their role in delivering a functional rental platform.

## 1. User Management
Handles user registration, login, and profile management. Users can either list properties as hosts or make bookings as guests, depending on their role.

## 2. Property Management
Allows hosts to add, update, and delete property listings. Each property includes details like title, location, pricing, and availability, making it visible to potential guests.

## 3. Booking System
Enables guests to book available properties for specific dates. The system ensures that bookings don’t overlap and that both parties can view booking details.

## 4. Payment Processing
Handles payment transactions tied to bookings. It ensures secure payments, updates booking statuses, and stores payment history.

## 5. Reviews and Ratings
Allows guests to leave feedback on properties they’ve stayed in. This helps other users make informed decisions and encourages quality service from hosts.

## 6. Search and Filtering *(optional but useful)*
Provides search functionality so users can find listings by location, price range, or availability. This improves the user experience when browsing properties.



