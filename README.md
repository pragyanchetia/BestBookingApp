<div align="center">

# BestBookingApp

### A full-stack hotel discovery and booking platform

**Search stays, explore hotel details, manage listings, and review your bookings in one application.**

[![React](https://img.shields.io/badge/React-18-20232A?logo=react)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-5-646CFF?logo=vite)](https://vitejs.dev/)
[![Express](https://img.shields.io/badge/Express-4-404D59?logo=express)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Mongoose-47A248?logo=mongodb)](https://www.mongodb.com/)
[![Playwright](https://img.shields.io/badge/E2E-Playwright-2EAD33?logo=playwright)](https://playwright.dev/)

</div>

---

## Overview

BestBookingApp is a full-stack hotel booking platform inspired by familiar travel-booking experiences. It pairs a React and TypeScript frontend with an Express API and MongoDB data layer.

Visitors can search and filter hotel listings, explore hotel detail pages, and complete a booking flow. Authenticated users can manage their own hotels and review their bookings.

## Features

- **Hotel search** — search for stays using the search form.
- **Filtering and pagination** — filter results by price, star rating, hotel type, and facilities; browse paginated results.
- **Hotel details** — view information and images for individual listings.
- **Booking flow** — collect guest information and display a booking summary.
- **User authentication** — registration, sign-in, sign-out, and authenticated API routes.
- **Booking management** — view personal bookings.
- **Hotel management** — create and edit listings with details, facilities, guest capacity, and images.
- **Image handling** — Cloudinary integration for hotel imagery.
- **Payment integration** — Stripe dependencies are included for payment-related functionality.
- **End-to-end testing** — Playwright test files cover hotel search and hotel management scenarios.

## Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | React, TypeScript, Vite |
| Styling / UI | Tailwind CSS, Headless UI, React Icons |
| Forms | React Hook Form |
| API | Node.js, Express, TypeScript |
| Database | MongoDB, Mongoose |
| Authentication | JWT, bcryptjs, cookie-parser |
| Images | Cloudinary |
| Payments | Stripe |
| Testing | Playwright |

## Architecture

```text
frontend/       React + TypeScript application (Vite)
backend/        Express REST API, MongoDB models, authentication and booking routes
e2e-tests/      Playwright browser tests
```

The backend is configured to serve the built frontend assets, so a production deployment can serve the application through the backend process.

## Getting Started

### Prerequisites

- Node.js and npm
- MongoDB connection string
- Cloudinary credentials for image upload
- Stripe keys if you enable payment-related functionality

### 1. Clone the repository

```bash
git clone https://github.com/pragyanchetia/BestBookingApp.git
cd BestBookingApp
```

### 2. Configure the backend

```bash
cd backend
npm install
```

Create a local environment file using the variable names expected by the backend code:

```env
MONGODB_CONNECTION_STRING=
JWT_SECRET_KEY=
FRONTEND_URL=http://localhost:5173
CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=
STRIPE_API_KEY=
```

Review the backend source for any additional required variables and use your own credentials.  

Start the backend in development mode:

```bash
npm run dev
```
 

### 3. Start the frontend

Open another terminal:

```bash
cd frontend
npm install
npm run dev
```

Vite prints the local development URL when it starts (typically [http://localhost:5173](http://localhost:5173)).

### 4. Build for production

Build the frontend first:

```bash
cd frontend
npm run build
```

Then compile the backend:

```bash
cd ../backend
npm run build
npm start
```

### 5. Run end-to-end tests

```bash
cd e2e-tests
npm install
npx playwright install
npx playwright test
```

The Playwright configuration includes Chromium, Firefox, and WebKit projects. Configure the test base URL and required test data to match your local environment.

## Project Structure

```text
frontend/src/
  components/     Search controls, filters, cards, layout
  forms/          Booking, guest information, hotel management forms
  pages/          Search, detail, booking, sign-in, account pages
  contexts/       App and search state
backend/src/
  routes/         Auth, users, hotels, and bookings API routes
e2e-tests/
  tests/          Browser-level test scenarios
```

## Author

[Pragyan Chetia](https://github.com/pragyanchetia)
