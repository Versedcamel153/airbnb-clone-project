# airbnb-clone-project
This project is a full-featured Airbnb clone designed to replicate the core functionality of the original platform. It allows users to list properties, browse listings, make bookings, communicate with hosts/guests, and manage stays — all in a modern, responsive interface. The goal is to build a scalable, secure, and user-friendly web app that demonstrates solid full-stack development practices.

## Project Goals
Recreate the essential features of Airbnb including user authentication, property management, and booking functionality.

Implement a clean and responsive UI with real-time interactions.

Learn and apply modern backend and frontend technologies in a practical project.

Build deployable, maintainable, and testable software using CI/CD practices.



# Team Roles
1. Backend Developer
2. Database Adminstrator
3. DevOps Engineer
4. QA Engineer


# Technology Stack
1. Django
2. Django REST Framework
3. PostgreSQL
4. GraphQL
5. Celery
6. Redis
7. Docker
8. CI/CD Pipelines

# Database Design
1. Users:
    - Full name: Name of the user.
    - Email: unique email addresses for each user.
    - Property: A user can have multiple properties.

2. Properties:
    - ID: Unique identifier for each  property.
    - User: Owner of the property.
    - Name: Name of property
    - Location: Property location.
    - Description: Brief description of the property
    - Price: Cost of the property.
    - Timestamp: Day and time of creation

3. Booking:
    - ID: Unique identifier for each booking.
    - Property: Each booking is related to a property.
    - Timestamp: Day and time of booking.

4. Review:
    - ID: Unique identifier for a review.
    - Property: Each review belongs to a property.
    - Comment: Comment of the review.
    - Stars: Stars assigned to the property(from 1-5 stars).

5. Payments:
    - Transaction ID: Unique identifier for the payment.
    - Amount: Total amount paid.
    - Timestamp: Day and time of payment.


# Feature Breakdown
### User management:
1. User registration, login, authentication and profile management.

### Property Management:
1. Enables hosts to create, update and delete their listings/properties

2. It is the core of the platform, giving hosts control over their rental offerings.

### Booking System:
1. Allows guest to check available properties, make reservations and receive confirmation.

2. This feature handles scheduling, availabilit conflicts, and booking history to ensure smooth transactions.

### Search and Filtering
1. Let users search for property by location, price range, dates, amenities, and property type.

2. Improves user experience by helping guests quickly find listings that match their preferences.

### Reviews and Ratings
1. User can leave feedback after a stay and rate their experience.

2. Builds trust on the platform and helps future users make informed decisions.

### Payment Integration
1. Support secure payment processing for bookings. 

2. Handles transactions, refunds, and payouts to hosts, ensuring both partied are protected.



# API Security
## Authentication
**Method:** Token-based authentication using JSON Web Tokens (JWT)

**Purpose:** Ensures that only verified users can access protected endpoints (e.g., booking a property or listing a rental).

**Why:** Prevents unauthorized access and impersonation by enforcing identity validation.

## Authorization
**Method:** Role-based access control (RBAC) to differentiate between guests, hosts, and admins.

**Purpose:** Limits actions users can perform based on their role — e.g., only hosts can create listings, and only admins can delete user accounts.

**Why:** Protects system integrity and enforces user-specific privileges to avoid abuse.

## Rate Limiting
**Method:** Throttling requests using a middleware like django-ratelimit or a proxy like Nginx or Cloudflare.

**Purpose:** Prevents API abuse by limiting the number of requests per user/IP within a time frame.

**Why:** Shields the platform from brute-force attacks, spamming, and denial-of-service (DoS) attempts.



## Secure Payment Handling
**Method:** Integration with trusted third-party payment gateways (e.g., Stripe).

**Purpose:** Outsources payment processing to avoid directly handling card data.

**Why:** Ensures compliance with PCI-DSS standards and minimizes liability.

# CI/CD Pipeline
CI/CD (Continuous Integration and Continuous Deployment) is a development practice that automates the process of testing, building, and deploying code. Every change pushed to the repository can trigger automated tests and deployments, ensuring code quality and faster delivery.

For this project, CI/CD helps reduce bugs, streamline updates, and maintain consistent production environments. It allows developers to focus on writing code while the pipeline handles testing and deployment.

Tools that can be used:

**GitHub Actions** – Automates testing and deployment workflows directly from GitHub.

**Docker** – Packages the app into a portable container for consistent deployments.

**Render / Heroku / Railway / AWS EC2** – Hosting platforms for live deployments.

**pytest / Jest / ESLint** – Tools for testing and code linting.