Link - https://test-task-psi-five.vercel.app/main
# Sports Center Booking System

## Overview

This is a full-stack web application that allows operations managers to manage sports center bookings across multiple cities in India. The application provides functionality for viewing and creating bookings for different sports offered at the centers, ensuring no double bookings occur. 

## Features

- **Select Centers**: Manage bookings for centers located in 13 cities across India, including Bengaluru, Mumbai, Delhi, etc.
- **Select Sports**: Available sports include Badminton, Squash, Tennis, Football, Cricket, and Basketball.
- **View Bookings**: Displays current bookings for each court/resource of a selected sport on a selected day.
- **Create Bookings**: Allows managers to book time slots for sports, ensuring no double booking conflicts for courts/resources.

## Tech Stack

### Backend
- **Node.js** with **Express.js**
- **MongoDB** for database management
- **Mongoose** as the ODM for MongoDB
- **Typescript** for type-safe backend development
- **CORS**, **body-parser**, and **dotenv** for API middleware

### Frontend
- Not provided in the current setup, but you can use **React.js** with **Axios** for making API requests and building the frontend.

### Deployment
- The app is configured to be deployed on **Vercel** as per the provided `vercel.json` configuration file.

## Project Structure

```
- src/
  - index.ts          // Main backend file where API routes are defined
- build/              // Compiled output from Typescript
- package.json        // Project dependencies and scripts
- tsconfig.json       // Typescript configuration
- .gitignore          // Git ignore file
- vercel.json         // Vercel deployment configuration
```

## Installation

### Prerequisites

Make sure you have **Node.js** and **npm** installed. You also need **MongoDB** for the database.

### Steps

1. **Clone the repository**:
   ```bash
   git clone <your-repository-url>
   ```

2. **Navigate to the project directory**:
   ```bash
   cd sports-center-booking-system
   ```

3. **Install dependencies**:
   ```bash
   npm install
   ```

4. **Set up environment variables**:

   Create a `.env` file in the root directory and add the following:
   ```
   MONGO_URI=<Your MongoDB Connection String>
   PORT=5000
   ```

5. **Run the app locally**:
   ```bash
   npm run build
   npm start
   ```

   The backend will be running on `http://localhost:5000`.

## API Endpoints

### View Bookings

- **Endpoint**: `GET /api/bookings`
- **Description**: Retrieves all bookings for a selected center, sport, and date.
- **Parameters**: 
  - `city`: The city where the booking is located.
  - `sport`: The sport for which bookings are being retrieved.
  - `date`: The date for which bookings are being retrieved.

### Create Booking

- **Endpoint**: `POST /api/bookings`
- **Description**: Creates a new booking for a selected court and time slot.
- **Body**:
  - `city`: The city of the center.
  - `sport`: The sport for the booking.
  - `court`: The court/resource being booked.
  - `date`: The date of the booking.
  - `time`: The time slot for the booking.
- **Validation**: Ensures no double bookings for the same court and time slot.

## Vercel Deployment

The project is configured to be deployed on **Vercel**. To deploy:

1. **Connect your repository** to Vercel.
2. Vercel will automatically use the `vercel.json` file to set up the build and deployment process.

## Dependencies

- **Express**: Fast, unopinionated, minimalist web framework for Node.js.
- **Mongoose**: Elegant MongoDB object modeling for Node.js.
- **CORS**: Middleware to enable Cross-Origin Resource Sharing.
- **Body-Parser**: Parse incoming request bodies in a middleware before your handlers.
- **Dotenv**: Loads environment variables from a `.env` file.
- **Typescript**: A strongly typed programming language that builds on JavaScript.

## License

This project is licensed under the **ISC License**.
