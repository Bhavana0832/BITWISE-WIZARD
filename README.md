# BITWISE-WIZARD
MovieStream: OOPS Project 
README

Overview
This is a simple Node.js application demonstrating the implementation of basic Object-Oriented Programming System (OOPS) principles in a backend server setup using Express.js and MongoDB. The project includes features such as user signup, login, and routing with database integration for persistent user management.


 Key Features

1. User Signup: 
   - Allows users to register by providing their first name, last name, email, and password.
   - Passwords are hashed using `bcrypt` for security.
   - Unique email validation prevents duplicate accounts.

2. User Login:
   - Authenticates users by comparing hashed passwords stored in the database.
   - Provides appropriate feedback for successful or failed login attempts.

3. Static File Serving:
   - Serves a `home.html` file as the root page of the application.

4. Database Integration:
   - Uses MongoDB for storing user data.
   - Managed through Mongoose models to implement an OOPS structure.


 Prerequisites
- Node.js installed on your system.
- MongoDB installed and running locally or accessible remotely.
- A basic understanding of Express.js and Mongoose.


 Installation

1. Clone the Repository:
  
   git clone BITWISE-WIZARD
   cd moviestream
   

2. Install Dependencies:
  
   npm install
  

3. Set Up MongoDB:
   - Ensure MongoDB is running locally or update the `mongoose.connect()` URI to point to your database.

4. Run the Server:

   node app.js
   
   The server will run on `http://localhost:3000` by default.


 Project Structure

moviestream/
│
├── public/                    Static files (HTML, CSS, JS)
│   ├── home.html              Home page
│   ├── login.html             Login page (placeholder, not implemented in this code)
│   └── signup.html            Signup page (placeholder, not implemented in this code)
│
├── app.js                     Main application logic
├── package.json               Project dependencies and scripts
└── README.md                  Project documentation



 API Endpoints
 1. POST /signup
- Description: Registers a new user.
- Request Body:
  json
  {
    "firstName": "Srikar",
    "lastName": "Reddy",
    "email": "srikarreddy@example.com",
    "password": "12345678"
  }

- Response:
  - Success: Redirects to the login page.
  - Error: Returns an appropriate error message (e.g., "User already exists").

 2. POST /login
- Description: Authenticates an existing user.
- Request Body:
  json
  {
    "email": "srikarreddy@example.com",
    "password": "12345678"
  }

- Response:
  - Success: Returns `{ "message": "Login successful" }`.
  - Error: Returns `{ "message": "Invalid email or password" }`.

 3. GET /
- Description: Serves the `home.html` file.


 Technologies Used
- Node.js: JavaScript runtime for building server-side applications.
- Express.js: Web framework for routing and middleware.
- MongoDB: Database for storing user data.
- Mongoose: ODM library for MongoDB.
- bcrypt: Library for hashing passwords.


 OOPS Principles Applied
1. Encapsulation:
   - User data is encapsulated within the `User` schema and model, restricting direct access.
2. Abstraction:
   - Abstracts database interactions using Mongoose models.
3. Polymorphism:
   - Dynamic response handling in routes (`res.send()`, `res.json()`, `res.redirect()`).
4. Inheritance:
   - While not directly applied in this example, Express middleware and Mongoose schema inheritance can be extended in more complex projects.


 Future Improvements
- Implement front-end HTML pages (`signup.html`, `login.html`).
- Add session handling for user authentication.
- Enhance error handling and validation.
- Deploy the application on a cloud platform.

