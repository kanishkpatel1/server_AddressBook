# Address Book Application

## Project Overview
This project consists of a **frontend** built with Angular and a **backend** built with Spring Boot. The backend requires additional setups including Redis, RabbitMQ, MySQL, Swagger, and Gmail app password authentication.

---

## Frontend Setup (Angular 17)

### Prerequisites
- **Node.js** and **npm** installed
- **Angular CLI** installed

### Steps to Run Frontend
1. Clone the repository:
   ```sh
   git clone https://github.com/kanishkpatel1/client_AddressBook.git
   cd client_AddressBook
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Run the application:
   ```sh
   ng serve
   ```
4. The frontend will be accessible at: [http://localhost:4200](http://localhost:4200)

---

## Backend Setup (Spring Boot)

### Prerequisites
Ensure you have installed and configured the following:
- **Redis**
- **RabbitMQ**
- **MySQL**
- **Swagger**
- **Gmail App Password** setup

### Steps to Configure Backend

1. **MySQL Configuration**
   - Update `application.properties` with your MySQL username and password.

2. **Gmail App Password Setup**
   - Enable 2-step verification in Gmail.
   - Generate an app password and update `application.properties`.

3. **Run the Backend**
   - Start the Spring Boot application.

4. **Create a User via Postman**
   - Send a `POST` request to register a new user:
     ```sh
     POST http://localhost:8080/api/auth/register
     ```
     **Request Body (JSON - raw):**
     ```json
     {
       "username": "your_username",
       "email": "your_email@example.com",
       "role": "USER",
       "password": "your_password"
     }
     ```

   - Send a `POST` request to login:
     ```sh
     POST http://localhost:8080/api/auth/login
     ```
     **Request Body (JSON - raw):**
     ```json
     {
       "username": "your_username",
       "password": "your_password"
     }
     ```

   - Upon successful login, you will receive a user ID.

5. **Update AddressBookController**
   - Modify `username` at **line 114** to match your registered username.
   - Update `id` at **line 139** (default is `1` for first-time setup).

---

## Final Steps
Once everything is set up, the frontend and backend will be fully functional.

Thank you!

**Regards,**  
*Kanishk Patel*

For any kind of help, contact me: **kanishkdeveshpatel@gmail.com**
