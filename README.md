# Todo Backend Installation Guide

This guide will help you set up a simple backend for a Todo application using Node.js, Express, and Prisma. The backend provides a RESTful API for managing tasks, including creating, reading, updating, and deleting tasks.

## Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js**: Version 18 or later
- **npm**: Version 9 or later
- **MySQL Database**: Ensure you have access to a MySQL database

## Installation Steps

1. **Clone the Repository**

   Begin by cloning the repository to your local machine:

   ```bash
   git clone https://github.com/fullstackdevelopment5505/todo-backend-devon.git
   ```

2. **Install Project Dependencies**

   Navigate to the project directory and install the necessary dependencies:

   ```bash
   npm install
   ```

3. **Database Configuration**

   Set up your database connection by following these steps:

   - Create a `.env` file in the root directory of the project.
   - Add your MySQL database connection string to the `.env` file in the following format:

     ```plaintext
     DATABASE_URL="mysql://user:password@localhost:3306/database_name"
     ```

4. **Run Database Migrations**

   Use Prisma to set up your database schema by running the following command:

   ```bash
   npx prisma migrate dev --name init
   ```

5. **Generate Prisma Client**

   Generate the Prisma client to interact with your database:

   ```bash
   npx prisma generate
   ```

## Running the Application

1. **Start the Server**

   Launch the server using the following command:

   ```bash
   npm start
   ```

   By default, the server will be accessible at `http://localhost:5000`.

2. **Available API Endpoints**

   The following endpoints are available for interacting with the Todo application:

   - `GET /tasks`: Retrieve all tasks.
   - `POST /tasks`: Create a new task. Requires `title` and `color` in the request body.
   - `GET /tasks/:id`: Retrieve a task by ID.
   - `PUT /tasks/:id`: Update a task by ID. Accepts `title`, `color`, and `completed` in the request body.
   - `DELETE /tasks/:id`: Delete a task by ID.

## Development Information

- **Scripts**

  - `npm start`: Use this script to start the server.

## Project Dependencies

- **Express**: A web framework for Node.js
- **Prisma**: A next-generation ORM for Node.js and TypeScript
- **CORS**: Middleware for enabling CORS
- **Body-Parser**: Middleware for parsing request bodies

## Author

- Devon Colomb
