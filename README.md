# Nxt Trendz Authentication App

This React app implements user authentication by connecting to a backend login API. Users can log in using valid credentials, and upon success, they are redirected to the Home route. Invalid login attempts show the error message returned from the API.

---

## Features

- **Login API Integration:**  
  Sends a POST request to the login API with username and password.  
  URL: `https://apis.ccbp.in/login`

- **Authentication Flow:**  
  - On successful login, stores JWT token in cookies and redirects to Home (`/`) route.  
  - On failed login, displays the error message returned from the API.  
  - Redirects already authenticated users trying to access `/login` back to `/`.

- **Routing:**  
  - `/login` — Login page (with form and error display).  
  - `/` — Home page (accessible only after authentication).

- **Logout Functionality:**  
  Logout button clears JWT token and redirects to `/login`.

---

## Live Demo

Check out the live app here: [https://MariTrendz.ccbp.tech](https://MariTrendz.ccbp.tech)

---

## Tech Stack

- **Frontend:**  
  - React (Functional and Class Components)  
  - React Router DOM (Routing)  
  - JavaScript (ES6+)  
  - CSS (Flexbox, Grid, Box Shadows)  
  - React Icons (for icons in UI)  

- **State Management:**  
  - React component state and props  

- **Authentication & Storage:**  
  - js-cookie (for storing and accessing JWT tokens in cookies)  

- **API:**  
  - RESTful API calls via Fetch API

- **Development Tools:**  
  - Node.js and npm  
  - Create React App (boilerplate)  

---

## API Requests & Responses

### Login API

- **Endpoint:** `https://apis.ccbp.in/login`
- **Method:** POST
- **Request Body:**
  ```json
  {
    "username": "rahul",
    "password": "rahul@2021"
  }

Success Response:

{
  "jwt_token": "jwt_token_string"
}
Failure Response:


{
  "error_msg": "Invalid username or password"
}

Implementation Details
LoginForm Component
Captures username and password inputs.

Calls login API on form submission.

Shows loader while waiting for the response.

On success: saves jwt_token in cookies and redirects to Home (/).

On failure: displays error message returned from API.

Home Component
Displays a welcome message and logout button.

Logout clears cookies and redirects to /login.

Header Component
Contains the app title and logout button (visible only when authenticated).

Protected Routing
Redirect unauthenticated users from Home route to /login.

Redirect authenticated users from /login to Home route.

Styling Tips
Used box-shadow for container styling.

Used cursor: pointer for buttons.

Used outline: none for input/button focus styling.

## Folder Structure

src/
  components/
    LoginForm/
      index.js
      index.css
    Home/
      index.js
      index.css
    Header/
      index.js
      index.css
  App.js
  index.js

## Author
Maridi Kumar Koneti

License
This project is licensed under the MIT License 



