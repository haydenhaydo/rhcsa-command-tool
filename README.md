# RHC_SA Command Tool

This project is a tool for practicing for the Red Hat Certified System Administrator (RHCSA) exam. It consists of a frontend web application and a backend API.

## Getting Started

You can run this project using Docker (recommended) or by running the frontend and backend services manually.

### With Docker

The simplest way to get started is with Docker Compose:

```bash
docker-compose up --build
```

This will build the images and start the frontend, backend, and database services. The application will be available at [http://localhost:3000](http://localhost:3000).

### Manual Setup

You can also run the frontend and backend services separately. This setup works out-of-the-box with no extra configuration.

**Backend:**

1.  Navigate to the `backend` directory: `cd backend`
2.  Install dependencies: `npm install`
3.  Start the server: `npm start` (The server will run on `http://localhost:5000`)

**Frontend:**

1.  Navigate to the `frontend` directory: `cd frontend`
2.  Install dependencies: `npm install`
3.  Start the development server: `npm start` (The app will open at `http://localhost:3000`)

The frontend is configured to automatically proxy API requests to the backend.
