# Express + PostgreSQL User API

## Setup Instructions

1. **Install Requirements**  
   - PostgreSQL  
   - Node.js

2. **Create Database**
   ```sql
   CREATE DATABASE your_database_name;
   \c your_database_name
   CREATE TABLE users (
     id SERIAL PRIMARY KEY,
     name VARCHAR(100),
     email VARCHAR(100),
     age INTEGER
   );
   ```

3. **Configure DB Connection**  
   Edit the `Pool` configuration in `index.js` to match your database credentials.

4. **Install Project Dependencies**
   ```bash
   npm install
   ```

5. **Run the Server**
   ```bash
   node index.js
   ```

## API Endpoints

| Method | Endpoint     | Description       |
|--------|--------------|-------------------|
| GET    | /users       | Get all users     |
| GET    | /users/:id   | Get user by ID    |
| POST   | /users       | Create new user   |
| PUT    | /users/:id   | Update user       |
| DELETE | /users/:id   | Delete user       |

## Example POST Body
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "age": 30
}
```
