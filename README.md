# Mini Expense Tracker with Intelligent Insights

## Overview
The **Mini Expense Tracker** is a web application that enables users to track their expenses, categorize spending, and gain insights through visualized reports. The app supports authentication, CRUD operations for expense management, and insightful analytics using charts.

## Features
### 1. Authentication
- JWT-based authentication with HTTP-only cookies.
- User registration with first name, last name, email, and password.
- Secure login/logout mechanism with token invalidation.
- Graceful handling of token expiry with refresh tokens.

### 2. Expense Management
- Users can **add, update, delete, and view** expenses.
- Each expense includes:
  - Amount (numeric, required)
  - Category (e.g., Food, Travel, etc.)
  - Date (required)
  - Description (optional)
- Pagination and filtering by date range and category.

### 3. Spending Insights
- Backend computes insights on:
  - **Total spending per category**
  - **Percentage distribution across categories**
- Frontend visualizations using **MUI X Charts** or **Recharts**.
- Efficient handling of large datasets.

### 4. Frontend (ReactJS + MUI/Shadcn)
- **Login/Registration Page**: Handles secure JWT authentication.
- **Dashboard**: Displays expenses with pagination and filtering.
- **Insights**: Showcasing spending breakdown with a bar/pie chart.
- **Expense Management**: Forms for adding/editing expenses and delete functionality.
- **Light & Dark Theme Support** (Bonus Feature)

### 5. Backend (NodeJS/Express or Python/FastAPI)
- **Secure API with JWT authentication** (HTTP-only cookies).
- **Expense CRUD operations**.
- **Optimized endpoints for spending insights**.
- **Pagination and filtering logic** for expense queries.

### 6. Database (MongoDB with Mongoose or PostgreSQL with Sequelize)
- Logical schema design.
- Query optimization for performance.

## Setup and Installation
### Prerequisites
- Node.js (if using Express) or Python (if using FastAPI)
- MongoDB/PostgreSQL
- Git
- Docker (optional for containerized setup)

### Backend Setup
```sh
# Clone the repository
git clone https://github.com/yourusername/mini-expense-tracker.git
cd mini-expense-tracker/backend

# Install dependencies (For NodeJS Backend)
npm install

# Configure environment variables
cp .env.example .env

# Start the backend server
npm start
```

### Frontend Setup
```sh
cd mini-expense-tracker/frontend

# Install dependencies
yarn install # or npm install

# Start the development server
yarn dev # or npm start
```

### Database Setup
For MongoDB:
```sh
# Run MongoDB
mongod --dbpath ./data
```

For PostgreSQL:
```sh
# Run PostgreSQL
docker-compose up -d
```

## API Documentation
### Authentication Endpoints
| Method | Endpoint | Description |
|--------|----------|--------------|
| POST | /api/auth/register | Register a new user |
| POST | /api/auth/login | User login |
| POST | /api/auth/logout | User logout |
| GET | /api/auth/refresh | Refresh token |

### Expense Management Endpoints
| Method | Endpoint | Description |
|--------|----------|--------------|
| GET | /api/expenses | Get all expenses with pagination & filters |
| POST | /api/expenses | Add a new expense |
| PUT | /api/expenses/:id | Update an expense |
| DELETE | /api/expenses/:id | Delete an expense |

### Spending Insights Endpoints
| Method | Endpoint | Description |
|--------|----------|------------------|
| GET | /api/insights | Get total and category-wise spending insights |

## Deployment
The app can be deployed using **AWS, Vercel, or Heroku**.
- Use **Docker** for containerized deployment.
- CI/CD pipelines can be set up using **GitHub Actions**.

## Tech Stack
### Frontend
- ReactJS (with MUI or Shadcn)
- MUI X Charts or Recharts (for graphs)

### Backend
- Node.js + Express (or Python + FastAPI)
- JWT Authentication with HTTP-only cookies

### Database
- MongoDB (Mongoose) or PostgreSQL (Sequelize)

### DevOps
- Docker
- AWS/Vercel/Heroku Deployment

## Contribution Guidelines
1. Fork the repository.
2. Create a new branch (`feature-branch`).
3. Commit your changes with proper messages.
4. Push and create a Pull Request.

## License
This project is licensed under the MIT License.

---

### 🚀 Happy Coding! 🎯

