User Notification Preferences API

A serverless API for managing user notification preferences and sending notifications.
This project enables efficient handling of user preferences for various notification types, delivery channels, and frequencies. Designed using Nest.js, 
the API is optimized for scalability, validation, and performance.

🚀Features
1.User Preferences Management

Create, read, update, and delete (CRUD) user notification preferences.
Support for multiple notification types: marketing, newsletters, updates.
Flexible delivery channels: email, SMS, and push notifications.
Timezone and frequency support for personalized notifications.

2.Notification Management

Simulate notification sending across channels.
Log notifications with delivery status and metadata.
Track notification statistics.

3.Serverless Deployment

Deployed using AWS Lambda for scalability and cost efficiency.

4.Robust Validation

Validate email format, timezone strings, and enums using class-validator.

5.API Design Best Practices

RESTful architecture.
Comprehensive error handling.
Proper HTTP status codes and responses.

6.Performance Enhancements

Basic rate limiting.
Request logging for debugging and analytics.

🛠️ Tech Stack

Framework: Nest.js
Database: MongoDB with Mongoose
Language: TypeScript
Validation: class-validator and class-transformer
Testing: Jest for unit and integration tests
Deployment: AWS Lambda / Vercel

📂 API Endpoints
User Preferences
Create Preferences
POST /api/preferences
Example Request:

json
Copy code
{
  "userId": "user123",
  "email": "user@example.com",
  "preferences": {
    "marketing": true,
    "newsletter": false,
    "updates": true,
    "frequency": "weekly",
    "channels": {
      "email": true,
      "sms": false,
      "push": true
    }
  },
  "timezone": "America/New_York"
}
Get Preferences
GET /api/preferences/:userId

Update Preferences
PATCH /api/preferences/:userId

Delete Preferences
DELETE /api/preferences/:userId

Notification Management
Send Notification
POST /api/notifications/send
Example Request:

json
Copy code
{
  "userId": "user123",
  "type": "marketing",
  "channel": "email",
  "content": {
    "subject": "Special Offer",
    "body": "Check out our latest deals!"
  }
}
Get Notification Logs
GET /api/notifications/:userId/logs

Get Notification Statistics
GET /api/notifications/stats

🧪 Testing
Unit Tests

Service layer and validation testing using Jest.
Mocked database operations for isolated testing.
Integration Tests

Full API endpoint tests to verify end-to-end functionality.
Tests for database interactions and rate limiting.

Run tests with:

npm run test

🌐 Deployment

Environment Variables
Create a .env file with the following variables:

MONGO_URI=<your-mongodb-uri>
PORT=3000

Deploy to AWS Lambda

1.Install Serverless Framework: npm install -g serverless
2.Deploy with: sls deploy

View Live API

Deployed API URL (Replace with your API URL)

📊 Example Use Case

1.Personalized Notification Preferences
A user can choose how frequently they want to receive notifications and via which channels (email, SMS, or push).

2.Efficient Notification Delivery
Marketers can send targeted notifications to users, respecting their preferences and timezones.

📄 Documentation

Swagger Documentation
Access at /api/docs for API specifications.

✨ Bonus Features
API Key Authentication
Add secure access control with API keys for client applications.

Notification Queueing Simulation
Simulate notification queues for scalable delivery.

Performance Monitoring
Integrated monitoring to track API performance.

📘 Getting Started
Clone the Repository

git clone https://docs.notificationapi.com/components/user-preferences
cd notification-preferences-api
Install Dependencies

npm install
Run Locally

npm run start:dev
Access the API

API: http://localhost:3000
Swagger Docs: http://localhost:3000/api/docs

🎯 Why This Project?
This project demonstrates clean architecture, scalable design, and real-world problem-solving skills. 
It highlights expertise in Nest.js, serverless deployment, and modern backend development practices,
making it a perfect showcase for recruiters seeking skilled developers.

📂 Repository Structure
sql

notification-preferences-api/
│
├── src/
│   ├── user-preferences/
│   │   ├── user-preferences.controller.ts
│   │   ├── user-preferences.service.ts
│   │   ├── schemas/
│   │   │   └── user-preference.schema.ts
│   │
│   ├── notifications/
│       ├── notifications.controller.ts
│       ├── notifications.service.ts
│       ├── schemas/
│           └── notification-log.schema.ts
│
├── test/
├── serverless.yml
├── package.json
└── README.md
🛡️ License
This project is licensed under the MIT License.

🤝 Contact
Feel free to reach out for any questions or collaboration:
Your Name:R JEYASHREE
Email:rjeyashree2003@gmail.com









