## Team Roles

### Backend Developer  
Responsible for designing and implementing server-side logic, APIs, and integrations with the database. Ensures that the backend processes requests correctly and efficiently.

### Database Administrator (DBA)  
Manages design, performance, maintenance and security of the database systems. Responsible for schema creation, data integrity, indexing, backup/restore and optimization.

### Frontend Developer  
Builds the user interface (UI) that communicates with the backend APIs. Ensures that the client side is responsive, usable and visual design meets project needs.

### DevOps / Infrastructure Engineer  
Sets up and maintains CI/CD pipelines, manages containerization (e.g., Docker), cloud deployment, monitoring and infrastructure scaling. Ensures smooth, automated deployment and operations.

### Project Manager  
Coordinates project timelines, divides tasks, monitors progress, ensures team collaboration, and communicates between stakeholders. Ensures project delivery aligns with goals and schedule.
## Technology Stack

### Backend Framework
**Django** — A Python-based web framework used to build the RESTful APIs that handle all application logic.

### Database
**PostgreSQL / MySQL** — Relational database used to store users, bookings, payments, and reviews.

### API Layer
**GraphQL / Django REST Framework** — Enables flexible data queries and efficient client-server communication.

### CI/CD Tools
**GitHub Actions** — Automates testing and deployment processes.  
**Docker** — Used to containerize the app for consistent environments.

### Security
**JWT (JSON Web Tokens)** — Used for authentication and session management.  
**HTTPS** — Ensures encrypted communication between client and server.
## Database Design

### Key Entities
1. **User**
   - id (Primary Key)
   - name
   - email
   - password
   - created_at

2. **Property**
   - id (Primary Key)
   - user_id (Foreign Key → User)
   - title
   - description
   - price_per_night
   - location

3. **Booking**
   - id (Primary Key)
   - user_id (Foreign Key → User)
   - property_id (Foreign Key → Property)
   - start_date
   - end_date
   - status

4. **Payment**
   - id (Primary Key)
   - booking_id (Foreign Key → Booking)
   - amount
   - payment_method
   - payment_status

5. **Review**
   - id (Primary Key)
   - user_id (Foreign Key → User)
   - property_id (Foreign Key → Property)
   - rating
   - comment

### Relationships
- One **User** can own multiple **Properties**
- One **User** can make multiple **Bookings**
- Each **Booking** belongs to one **User** and one **Property**
- Each **Booking** has one **Payment**
- One **User** can leave multiple **Reviews**
## Feature Breakdown

### 1. User Management
Handles user registration, login, profile updates, and authentication.

### 2. Property Management
Allows property owners to list new properties, upload details, and manage availability.

### 3. Booking System
Enables users to book available properties, manage reservations, and view booking history.

### 4. Payment Integration
Handles payment processing, refunds, and transaction history securely.

### 5. Reviews and Ratings
Allows guests to leave feedback and ratings for properties after stays.

### 6. Admin Dashboard
Provides administrators tools to manage users, properties, and reports.
