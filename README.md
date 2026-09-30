# 🍔 Zosh Food – Online Food Delivery Platform

Zosh Food is a full-stack **online food delivery application** built using **React, Spring Boot and MySQL**.

The idea behind this project is simple: customers can discover restaurants, browse food items, add their favourite food to a cart and place orders. On the other side, restaurant and admin users can manage restaurants, food items, categories and orders.

I built this project to understand how a real-world full-stack application works from the frontend all the way to the backend and database.

---

## 📸 Project Preview

### 🏠 Home Page

The home page allows users to explore restaurants and start looking for food.

### 🍕 Restaurant & Food Menu

Users can open a restaurant and browse the available food items.

### 🛒 Cart & Checkout

After selecting food, users can review their cart and continue with the ordering process.

### 👨‍💼 Admin / Restaurant Dashboard

Restaurant and admin users can manage restaurant information, food items, categories and orders.

---

# ✨ Features

## 👤 Customer

- Create an account and log in
- JWT-based authentication
- Browse restaurants
- Search for food and restaurants
- View restaurant details
- Browse food menus
- Add food items to cart
- Update cart items
- Remove items from cart
- Manage delivery addresses
- Place food orders
- View previous orders
- Check order status
- Add reviews and ratings
- Manage favourite restaurants/food
- Receive notifications
- Manage profile information
- Reset password

---

## 🏪 Restaurant / Admin

Restaurant users can manage their restaurant from the dashboard.

- Add restaurant information
- Update restaurant information
- Manage food items
- Add new food
- Update food
- Delete food
- Manage food categories
- Manage ingredients
- Manage ingredient categories
- View customer orders
- Update order information
- View restaurant-related information
- Manage restaurant events

---

## 👑 Super Admin

The application also contains functionality for a super administrator.

- Manage restaurants
- Review restaurant requests
- Manage users
- View restaurant information
- Access administrative dashboard

---

# 💳 Payment Integration

The project contains payment integration for online food ordering.

Payment-related integrations include:

- **Razorpay**
- **Stripe**

These integrations allow the application to be extended into a complete online ordering and payment system.

> For local development, use your own test API keys. Never upload real payment credentials to GitHub.

---

# 📧 Email & Notifications

The backend also contains functionality related to email and notifications.

These can be used for things such as:

- Order confirmation
- Password reset
- Order updates
- User notifications

---

# 🛠️ Technologies Used

### Frontend

- React
- JavaScript
- React Router
- Redux
- Redux Thunk
- Axios
- Material UI
- Styled Components
- Tailwind CSS
- Formik
- Yup

### Backend

- Java
- Spring Boot
- Spring MVC
- Spring Security
- JWT
- Spring Data JPA
- Hibernate
- REST APIs
- Maven

### Database

- MySQL

### Payment

- Razorpay
- Stripe

### Email

- Spring Boot Mail
- SMTP

---

# 🏗️ Project Architecture

The project follows a basic full-stack architecture where the React frontend communicates with the Spring Boot backend through REST APIs.

```text
                ┌──────────────────────┐
                │      React App       │
                │      Frontend        │
                └──────────┬───────────┘
                           │
                           │ REST API
                           ▼
                ┌──────────────────────┐
                │     Spring Boot      │
                │       Backend        │
                └──────────┬───────────┘
                           │
                ┌──────────┴───────────┐
                │                      │
                ▼                      ▼
        ┌──────────────┐       ┌──────────────┐
        │ Spring       │       │ Spring       │
        │ Security/JWT │       │ Services     │
        └──────────────┘       └──────┬───────┘
                                      │
                                      ▼
                              ┌──────────────┐
                              │    MySQL     │
                              │   Database   │
                              └──────────────┘
```

---

# 📂 Project Structure

```text
Zosh-Food
│
├── Source
│   │
│   ├── backend-spring boot
│   │   │
│   │   ├── src
│   │   │   └── main
│   │   │       ├── java
│   │   │       │   └── com
│   │   │       │       └── zosh
│   │   │       │           ├── config
│   │   │       │           ├── controller
│   │   │       │           ├── dto
│   │   │       │           ├── Exception
│   │   │       │           ├── model
│   │   │       │           ├── repository
│   │   │       │           ├── request
│   │   │       │           ├── response
│   │   │       │           └── service
│   │   │       │
│   │   │       └── resources
│   │   │
│   │   └── pom.xml
│   │
│   ├── frontend-react
│   │   │
│   │   ├── public
│   │   ├── src
│   │   │   ├── Admin
│   │   │   ├── SuperAdmin
│   │   │   ├── customers
│   │   │   ├── Routers
│   │   │   ├── State
│   │   │   ├── config
│   │   │   └── theme
│   │   │
│   │   └── package.json
│   │
│   ├── Zosh Food.postman_collection.json
│   └── Set Project on your local machine.txt
│
└── README.md
```

---

# 🔄 How the Application Works

The basic customer flow is:

```text
Register / Login
       ↓
Browse Restaurants
       ↓
Select Restaurant
       ↓
View Food Menu
       ↓
Select Food
       ↓
Add Food to Cart
       ↓
Select Address
       ↓
Checkout
       ↓
Payment
       ↓
Place Order
       ↓
Track / View Order
```

Restaurant/admin flow:

```text
Admin / Restaurant Login
          ↓
     Dashboard
          ↓
 ┌────────┼──────────┐
 ↓        ↓          ↓
Restaurant Food     Orders
Management          Management
 ↓        ↓          ↓
Details  Categories Status
```

---

# 🔐 Authentication & Security

The backend uses **Spring Security and JWT authentication**.

The basic flow is:

```text
User Login
    ↓
Backend verifies credentials
    ↓
JWT Token generated
    ↓
Token sent to frontend
    ↓
Frontend sends token with API requests
    ↓
Spring Security validates token
    ↓
Authorized request
```

Different parts of the application can be protected based on the user's role.

---

# 🗃️ Main Modules

The backend contains different modules for handling the major parts of the application.

### Authentication

- Registration
- Login
- JWT authentication
- Password reset

### Restaurant

- Restaurant management
- Restaurant information
- Restaurant status
- Restaurant events

### Food

- Food management
- Food categories
- Ingredients
- Ingredient categories

### Cart

- Add food
- Remove food
- Update quantity
- View cart

### Orders

- Create orders
- Order items
- Order status
- Order history

### Payments

- Razorpay
- Stripe

### Reviews

- Customer reviews
- Ratings

### Notifications

- User notifications
- Order-related notifications

---

# 🧪 Testing APIs with Postman

A Postman collection is included in the project:

```text
Source/Zosh Food.postman_collection.json
```

You can import this file into **Postman** and test the backend APIs after starting the Spring Boot application.

---

# ⚙️ Requirements

Before running the project, make sure you have installed:

- Java 17+
- Node.js
- npm
- MySQL
- Git
- Maven
- Postman (optional, for API testing)

---

# 🚀 How to Run the Project

## 1. Clone the Repository

```bash
git clone https://github.com/vinaykumar2004vinay/Online-Food-Delivery-Platform.git
```

Then:

```bash
cd Online-Food-Delivery-Platform
```

---

# 🗄️ 2. Create MySQL Database

Open MySQL and create a database.

```sql
CREATE DATABASE zosh_food;
```

Then configure your database username and password in:

```text
backend-spring boot/src/main/resources/application.properties
```

Example:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/zosh_food
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD
```

Use your own password.

---

# ☕ 3. Start Spring Boot Backend

Open a terminal and move into the backend folder:

```bash
cd "Source/backend-spring boot"
```

For Windows:

```bash
mvnw.cmd spring-boot:run
```

For Linux/macOS:

```bash
./mvnw spring-boot:run
```

The backend will start on the configured Spring Boot port.

---

# ⚛️ 4. Start React Frontend

Open another terminal:

```bash
cd Source/frontend-react
```

Install dependencies:

```bash
npm install
```

Start the application:

```bash
npm start
```

The React application will then open in your browser.

---

# 🔑 Environment Variables

If you use payment, email or other external services, configure the required credentials locally.

For example:

```text
RAZORPAY_API_KEY=your_key
RAZORPAY_API_SECRET=your_secret

STRIPE_API_KEY=your_key

MAIL_USERNAME=your_email
MAIL_PASSWORD=your_app_password
```

### ⚠️ Important

Do **not** push real API keys, passwords or secret credentials to GitHub.

Add sensitive files to `.gitignore` whenever necessary.

---

# 📚 What I Learned From This Project

While working on this project, I got practical experience with:

- Building a React frontend
- Creating REST APIs using Spring Boot
- Connecting React with Spring Boot
- Working with MySQL
- Using Spring Data JPA
- Implementing JWT authentication
- Working with Spring Security
- Managing application state with Redux
- Handling forms and validation
- Building customer and admin dashboards
- Creating a shopping cart
- Managing orders
- Working with payment gateways
- Testing APIs using Postman
- Organizing a large full-stack project

---

# 🔮 Future Improvements

There are several things that can be added in future versions:

- Docker support
- CI/CD using GitHub Actions
- Cloud deployment
- Real-time order tracking
- Delivery partner module
- Improved search and filtering
- More automated tests
- Better mobile responsiveness
- Restaurant analytics
- Improved notification system
