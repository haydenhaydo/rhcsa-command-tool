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

You can also run the frontend and backend services separately.

**Backend:**

1.  Navigate to the `backend` directory: `cd backend`
2.  Install dependencies: `npm install`
3.  Start the server: `npm start`

**Frontend:**

1.  Navigate to the `frontend` directory: `cd frontend`
2.  Install dependencies: `npm install`
3.  Start the development server: `npm start`

## Configuration

### Backend CORS Configuration

When running the services manually, the frontend and backend will be on different origins (`localhost:3000` and `localhost:5000`). To allow them to communicate, you must configure Cross-Origin Resource Sharing (CORS) for the backend.

1.  Create a `.env` file in the `backend` directory.
2.  Add the following line to the `.env` file:

    ```
    CORS_ALLOWED_ORIGIN=http://localhost:3000
    ```

This tells the backend to accept requests from the frontend's origin. When running with Docker, this variable is not needed, as the Nginx proxy handles requests.

### Frontend API Configuration

When running the frontend manually, you need to tell it the base URL of the backend API.

1.  Create a `.env` file in the `frontend` directory.
2.  Add the following line to the `.env` file:

    ```
    REACT_APP_API_BASE_URL=http://localhost:5000
    ```

This tells the frontend to send API requests to `http://localhost:5000`. When running with Docker, this variable is not needed, as the requests are proxied by Nginx.
