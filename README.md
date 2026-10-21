 <div align="center">

# BestBookingApp

### A Full-Stack Hotel Discovery and Booking Platform

**Search stays, explore hotel details, manage listings, and review your bookings in one application.**

[![Live Demo](https://img.shields.io/badge/Live-Demo-2ea44f?style=for-the-badge)](https://bestbooking.onrender.com/)

[![React](https://img.shields.io/badge/React-18-20232A?logo=react)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-5-646CFF?logo=vite)](https://vitejs.dev/)
[![Express](https://img.shields.io/badge/Express-4-404D59?logo=express)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Mongoose-47A248?logo=mongodb)](https://www.mongodb.com/)
[![Playwright](https://img.shields.io/badge/E2E-Playwright-2EAD33?logo=playwright)](https://playwright.dev/)

</div>

---

## Live Demo

**Explore the deployed application:** [BestBookingApp — Live Website](https://bestbooking.onrender.com/)

Visit the live website to explore hotel listings, try the search experience, and navigate the booking and hotel management features.

---

## Overview

BestBookingApp is a full-stack hotel discovery and booking platform inspired by modern travel-booking applications. It combines a responsive React and TypeScript frontend with a Node.js and Express backend, using MongoDB for data storage.

The application allows visitors to discover accommodation options, filter hotel listings, explore individual hotel details, and proceed through a booking flow. Authenticated users can manage their hotel listings and review their bookings.

The project demonstrates full-stack web development concepts, including REST API integration, authentication, database modeling, image uploads, form handling, and end-to-end testing.

## Features

- **Hotel Search:** Search for accommodation using the search form.
- **Filtering and Pagination:** Refine hotel results by price, star rating, hotel type, and facilities, and navigate through paginated listings.
- **Hotel Details:** Explore individual hotel listings, including descriptions, images, facilities, and other available information.
- **Booking Flow:** Enter guest information and review booking details.
- **User Authentication:** Register, sign in, sign out, and access protected API routes.
- **Booking Management:** View personal booking information.
- **Hotel Management:** Create and edit hotel listings, including details, facilities, guest capacity, and images.
- **Image Uploads:** Integrate Cloudinary for hotel image storage and management.
- **Payment Integration:** Include Stripe dependencies for payment-related functionality.
- **End-to-End Testing:** Use Playwright to test key user workflows, including hotel search and hotel management.

## Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | React, TypeScript, Vite |
| Styling and UI | Tailwind CSS, Headless UI, React Icons |
| Forms | React Hook Form |
| Backend | Node.js, Express, TypeScript |
| Database | MongoDB, Mongoose |
| Authentication | JWT, bcryptjs, cookie-parser |
| Image Management | Cloudinary |
| Payments | Stripe |
| Testing | Playwright |
| Deployment | Render |

## Architecture

The application follows a client-server architecture, separating the frontend, backend API, database layer, and browser-based tests.

```text
BestBookingApp/
├── frontend/
│   └── React + TypeScript + Vite
│       ├── components/
│       ├── forms/
│       ├── pages/
│       └── contexts/
│
├── backend/
│   └── Node.js + Express + TypeScript
│       └── src/
│           ├── routes/
│           ├── models/
│           └── ...
│
└── e2e-tests/
    └── Playwright browser tests
```

The backend is configured to serve the built frontend assets, allowing the application to be deployed as a single production application through the backend process.

## Getting Started

Follow these steps to run the project locally.

### Prerequisites

Make sure you have the following installed or configured:

- [Node.js](https://nodejs.org/) and npm
- A MongoDB database or MongoDB connection string
- A Cloudinary account for image uploads
- Stripe API credentials if payment functionality is enabled
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/pragyanchetia/BestBookingApp.git
cd BestBookingApp
```

### 2. Configure the Backend

Navigate to the backend directory and install the dependencies.

```bash
cd backend
npm install
```

Create a `.env` file in the backend directory and configure the environment variables expected by the application.

```env
MONGODB_CONNECTION_STRING=
JWT_SECRET_KEY=
FRONTEND_URL=http://localhost:5173

CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=

STRIPE_API_KEY=
```

Replace the empty values with your own credentials.

Check the backend source code for any additional required environment variables. Variable names must match those referenced in the application.

Start the backend development server:

```bash
npm run dev
```

### 3. Configure and Start the Frontend

Open a new terminal and navigate to the frontend directory.

```bash
cd frontend
npm install
npm run dev
```

Vite will display the local development URL, typically:

`http://localhost:5173`

Open that URL in your browser to access the application.

### 4. Build for Production

Build the frontend first:

```bash
cd frontend
npm run build
```

Then build and start the backend:

```bash
cd ../backend
npm run build
npm start
```

Ensure that the frontend build output directory matches the location configured in the backend's static-file serving setup.

### 5. Run End-to-End Tests

Navigate to the test directory:

```bash
cd e2e-tests
npm install
npx playwright install
```

Run the tests:

```bash
npx playwright test
```

To run tests with the Playwright UI:

```bash
npx playwright test --ui
```

The Playwright configuration includes Chromium, Firefox, and WebKit projects. Ensure that the application is running, the test base URL is configured correctly, and any required test data is available.

## Project Structure

The following is a simplified overview of the primary application directories.

```text
BestBookingApp/
├── frontend/
│   └── src/
│       ├── components/    # Search controls, filters, cards, layout
│       ├── forms/         # Booking and hotel management forms
│       ├── pages/         # Search, details, authentication, account
│       └── contexts/      # Application and search state
│
├── backend/
│   └── src/
│       ├── routes/        # Authentication, users, hotels, bookings
│       ├── models/        # Database models
│       └── ...
│
└── e2e-tests/
    └── tests/             # Browser-level test scenarios
```

## Deployment

BestBookingApp is deployed on Render.

- **Live application:** [https://bestbooking.onrender.com/](https://bestbooking.onrender.com/)
- **Hosting platform:** [Render](https://render.com/)

The production deployment uses the backend to serve the built frontend assets. Configure the required environment variables in the Render service settings, including the database connection, authentication secret, and any third-party service credentials required by the enabled features.

For deployment troubleshooting, verify the build commands, start command, static asset paths, environment variables, and database connectivity.

*Note:* The live application may take a little time to respond if the hosting service is using a free instance that has gone idle.

## Key Learning Outcomes

This project provides practical experience with:

- Building a full-stack application using React, TypeScript, Node.js, and Express.
- Designing and integrating REST APIs.
- Connecting a web application to MongoDB using Mongoose.
- Implementing authentication and protected routes.
- Building reusable UI components and form workflows.
- Handling image uploads with a third-party cloud service.
- Structuring frontend and backend code for maintainability.
- Testing browser workflows with Playwright.
- Building and deploying a full-stack application.

## Future Improvements

Potential enhancements include:

- Improving booking availability and reservation validation.
- Completing and testing the end-to-end payment workflow.
- Adding automated test coverage for authentication and booking operations.
- Improving error handling, loading states, and accessibility.
- Adding booking confirmation notifications and an administrative dashboard.

## Author

**Pragyan Chetia**

- GitHub: [@pragyanchetia](https://github.com/pragyanchetia)
- Live Project: [BestBookingApp](https://bestbooking.onrender.com/)

---

*Built with React, TypeScript, Node.js, Express, and MongoDB.*
