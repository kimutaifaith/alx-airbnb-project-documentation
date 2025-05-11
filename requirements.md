🛡️ 1. User Authentication
📌 Feature Overview
Enable users to register, log in, and manage sessions securely.

🔗 API Endpoints
POST /api/auth/register — Register a new user (guest or host)

POST /api/auth/login — Authenticate user and return JWT

GET /api/auth/profile — Retrieve authenticated user profile

PUT /api/auth/profile — Update user profile details

✅ Validation Rules
Email must be valid and unique

Password must be at least 8 characters

Role must be either “guest” or “host”

⚙️ Performance Criteria
Registration and login should respond in less than 1.5 seconds

Token should expire after 24 hours

🏘️ 2. Property Management
📌 Feature Overview
Allows hosts to create, update, view, and delete property listings.

🔗 API Endpoints
POST /api/properties/ — Create new property listing

GET /api/properties/:id — View property details

PUT /api/properties/:id — Edit a property

DELETE /api/properties/:id — Delete a property

✅ Validation Rules
Title must be at least 10 characters

Price must be a positive number

At least one availability date is required

Only authenticated hosts can create or modify listings

⚙️ Performance Criteria
Listing creation should complete within 2 seconds

Listing retrieval should support pagination (e.g., 10 per page)

📅 3. Booking System
📌 Feature Overview
Manages booking creation, status tracking, and cancellations.

🔗 API Endpoints
POST /api/bookings/ — Create a booking

GET /api/bookings/:id — View booking information

PUT /api/bookings/:id/cancel — Cancel a booking

✅ Validation Rules
Booking dates must be valid and available

Guests cannot book their own properties

Check-out date must be after check-in date

⚙️ Performance Criteria
System must prevent double booking using validation or locking

Booking confirmation should be processed in under 2 seconds
