# SUBY - Vendor Dashboard (Full Stack Project)

SUBY is a full-stack **Vendor Dashboard** application that allows vendors to manage their firms and products. It includes both **frontend** (React.js) and **backend** (Node.js, Express.js, MongoDB) components. Vendors can register, log in, add firms, add products, and manage their inventory through an intuitive user interface.

---

## Features

### Frontend (React.js)
- **User Authentication**: Vendors can register and log in.
- **Firm Management**: Add and manage firms.
- **Product Management**: Add, view, and delete products.
- **Responsive Design**: The dashboard is designed to be user-friendly and responsive.
- **Image Upload**: Upload images for firms and products.
- **Dynamic Routing**: Navigate between different sections of the dashboard.

### Backend (Node.js, Express.js, MongoDB)
- **Vendor Management**: Register, log in, and retrieve vendor details.
- **Firm Management**: Add and delete firms.
- **Product Management**: Add, retrieve, and delete products.
- **Authentication**: Secure endpoints using JWT (JSON Web Tokens).
- **File Uploads**: Handle image uploads for firms and products.
- **Database**: MongoDB for storing vendor, firm, and product data.

---

## Project Structure

### Frontend
```
DASHBOARD
├── node_modules
├── public
├── src
│   ├── vendorDashboard
│   │   ├── components
│   │   │   ├── forms
│   │   │   │   ├── AddFirm.jsx
│   │   │   │   ├── AddProduct.jsx
│   │   │   │   ├── Login.jsx
│   │   │   │   ├── Register.jsx
│   │   │   │   ├── VendorLogin.jsx
│   │   │   │   └── VendorRegister.jsx
│   │   │   ├── AllProducts.jsx
│   │   │   ├── NavBar.jsx
│   │   │   ├── NotFound.jsx
│   │   │   ├── SideBar.jsx
│   │   │   └── Welcome.jsx
│   │   ├── helpers
│   │   │   └── ApiPath.js
│   │   ├── pages
│   │   │   └── LandingPage.jsx
│   ├── App.css
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
└── index.html
```

### Backend
```
BACKEND
├── Controllers
│   ├── firmController.js
│   ├── productController.js
│   ├── vendorController.js
├── middlewares
│   └── verifyToken.js
├── models
│   ├── Firm.js
│   ├── Product.js
│   └── Vendor.js
├── node_modules
├── routes
│   ├── firmRoutes.js
│   ├── productRoutes.js
│   └── vendorRoutes.js
├── uploads
├── .env
├── .gitignore
├── classes.json
├── data.json
├── index.js
├── package-lock.json
└── package.json
```

---

## Installation

### Frontend
1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm run dev
   ```

### Backend
1. Navigate to the backend directory:
   ```bash
   cd backend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file in the root directory and add the following environment variables:
   ```env
   WhatIsYourName=your_secret_key
   MONGO_URI=your_mongodb_connection_string
   ```
4. Start the server:
   ```bash
   npm start
   ```

---

## Usage

### Frontend
- **Login/Register**: Use the login and register forms to authenticate.
- **Add Firm**: Navigate to the "Add Firm" section to add a new firm.
- **Add Product**: Navigate to the "Add Product" section to add a new product.
- **View Products**: Navigate to the "All Products" section to view and manage products.

### Backend
- **Vendor Registration**: Use the `/register` endpoint to register a new vendor.
- **Vendor Login**: Use the `/login` endpoint to log in a vendor and receive a JWT token.
- **Add Firm**: Use the `/add-firm` endpoint to add a new firm (requires authentication).
- **Add Product**: Use the `/add-product/:firmId` endpoint to add a new product to a firm.
- **Retrieve Products**: Use the `/:firmId/products` endpoint to retrieve all products for a firm.
- **Delete Product**: Use the `/:productId` endpoint to delete a product by ID.

---

## API Endpoints

### Vendor Routes
- **POST /register**: Register a new vendor.
- **POST /login**: Log in a vendor.
- **GET /all-vendors**: Retrieve all vendors.
- **GET /single-vendor/:apple**: Retrieve a single vendor by ID.

### Firm Routes
- **POST /add-firm**: Add a new firm (protected route).
- **DELETE /:firmId**: Delete a firm by ID.

### Product Routes
- **POST /add-product/:firmId**: Add a new product to a firm.
- **GET /:firmId/products**: Retrieve all products for a firm.
- **DELETE /:productId**: Delete a product by ID.

---

## Dependencies

### Frontend
- **React.js**: JavaScript library for building user interfaces.
- **React Router**: For routing and navigation.
- **React Loader Spinner**: For loading animations.
- **Axios**: For making HTTP requests.

### Backend
- **Express.js**: Web framework for Node.js.
- **Mongoose**: MongoDB object modeling for Node.js.
- **Multer**: Middleware for handling file uploads.
- **Bcryptjs**: Library for hashing passwords.
- **Jsonwebtoken**: Library for generating and verifying JWT tokens.
- **Dotenv**: Loads environment variables from a `.env` file.

---

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

## Acknowledgments

- **React.js** for frontend development.
- **Node.js** and **Express.js** for backend development.
- **MongoDB** for database management.
- **Multer** for handling file uploads.
- **Bcryptjs** and **Jsonwebtoken** for authentication.
