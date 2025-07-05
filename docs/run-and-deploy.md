# Running and Deploying the Application

This document provides instructions on how to run the application locally for development and testing purposes.

## Prerequisites

- Docker Desktop installed and running.
- A tool for making API requests, such as Postman or curl.

## Local Development Environment

The application is containerized using Docker and can be run locally using `docker-compose`.

### 1. Start the Application

To start the application, run the following command from the root of the project directory:

```bash
docker-compose up --build
```

This command will build the Docker images and start the backend server, PostgreSQL database, and Redis cache.

### 2. Verify the Application is Running

Once the containers are running, you can verify that the application is running by sending a GET request to `http://localhost:3000`.

You should receive a response with the text "Hello from 10-4 backend!".

### 3. Testing with Postman

You can use the provided Postman collection in `tests/postman/user.json` to test the user-related endpoints. The collection includes requests for creating and authenticating users.

To test the user creation endpoint, send a POST request to `http://localhost:3000/api/users` with a JSON body like the following:

```json
{
  "username": "driverjoe",
  "password": "securepass123",
  "displayName": "Joe the Driver"
}
```

### 4. Stopping the Application

To stop the application, press `Ctrl+C` in the terminal where `docker-compose` is running, and then run the following command:

```bash
docker-compose down
```
