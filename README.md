# RHCSA Command Tool

This project is a tool for practicing for the Red Hat Certified System Administrator (RHCSA) exam. It consists of a frontend web application and a backend API.

## Getting Started

You can run this project using Docker or by running the frontend and backend services manually.

### With Docker

The simplest way to get started is with Docker Compose:

Clone the repository and then cd into it and run:
```bash
docker-compose up -d --build
```

This will build the images and start the frontend, backend, and database services. The application will be available at [http://localhost:3000](http://localhost:3000).

### Manual Setup

You can also run the frontend and backend services separately. This requires having a MongoDB server installed and running on your local machine.

**Backend:**

1.  **Start MongoDB:** Ensure your local MongoDB server is running. You can typically start it by running the `mongod` command in a separate terminal.
2.  **Navigate to Backend:** Open a new terminal and navigate to the `backend` directory.
3.  **Install Dependencies:** `npm install`
4.  **Seed the Database:** Load the questions into the database by running: `npm run seed`
5.  **Start the Server:** `npm start` (The server will run on `http://localhost:5000`)

**Frontend:**

1.  **Navigate to Frontend:** In a separate terminal, navigate to the `frontend` directory: `cd frontend`
2.  **Install Dependencies:** `npm install`
3.  **Start the Development Server:** `npm start` (The app will now be available at `http://localhost:3000`)

The frontend is configured to automatically proxy API requests to the backend in this configuration.
