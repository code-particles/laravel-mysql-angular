**Technical Interview Task: Full-Stack Development with Laravel, MySQL, and Angular**

**Overview:**  
The goal of this technical exercise is to assess your ability to develop a simple API using Laravel, implement JWT-based authentication, and expose endpoints for customers and products. You will also build a simple Angular app to interact with the API.

### **Backend: Laravel API Development**

1. **Setup Laravel API:**

   - Create a Laravel project from scratch using Composer. Ensure it’s configured to connect to a MySQL database.
   - Set up the database migrations for the following tables:
     - **users**: For authentication, with fields like `id`, `name`, `email`, `password`.
     - **products**: Store product data with fields like `id`, `name`, `description`, `price`.
     - **customers**: Store customer data with fields like `id`, `name`, `email`, `phone_number`.

2. **Authentication (JWT-based login):**

   - Implement user authentication using Laravel and **JWT (JSON Web Token)**.
   - On successful login (with email/password), return a JWT token that can be used for further requests.
   - Install the **tymon/jwt-auth** package to manage JWT in Laravel.
     - Endpoint: **POST /api/login** to accept email and password, and return the JWT token.

3. **Protected Endpoint: Customers**

   - Create a **protected endpoint** for accessing customer data.
   - Only authenticated users should access this endpoint.
     - Endpoint: **GET /api/customers** to return a list of customers. This endpoint should only be accessible if the user provides a valid JWT in the request headers.

4. **Public Endpoint: Products**
   - Create a **public endpoint** for viewing products.
   - This endpoint should be accessible without authentication.
     - Endpoint: **GET /api/products** to return a list of products.

### **Frontend: Angular App**

5. **Frontend Setup:**

   - Create a simple **Angular** app to interact with the Laravel API.
   - Use Angular’s HTTP client module to make requests to the backend.

6. **Login Form:**

   - Create a basic login form in Angular that accepts email and password.
   - Upon successful login, store the JWT token and display a success message. Use the stored JWT token for further API requests.

7. **Display Products:**

   - Fetch and display the products from the public products endpoint using Angular.
   - No authentication should be required to access this section.

8. **Display Customers (Protected Data):**
   - Implement a feature that fetches and displays the customer list from the protected endpoint.
   - Ensure that the stored JWT token is passed in the headers when accessing this endpoint.
   - If the token is invalid or missing, display an appropriate error message.

---

### **Evaluation Criteria:**

- **API Design:** Clarity and correctness of the API implementation (routes, controllers, and models).
- **Authentication:** Proper JWT implementation and token management.
- **Security:** Secure handling of authentication and authorization.
- **Code Quality:** Structure, readability, and use of best practices.
- **Frontend Integration:** Ability to consume the API using Angular and proper state management (handling the token).
- **Bonus:** If the candidate can implement error handling for invalid logins or token expiration.

### **Submission Guidelines:**

While we will get a chance to interact on the live session over your work, eventually, please:

- Push the Laravel API to a GitHub repository with instructions on setting up the project.
- Push the Angular project to a separate GitHub repository with instructions.
- Share the repository links for review.
