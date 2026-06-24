# 🛒 E-Commerce Backend API

A scalable and secure **E-Commerce Backend System** built with **NestJS**, **MongoDB**, and modern backend architecture best practices. The system implements a complete e-commerce workflow including authentication, product management, cart, orders, coupons, payments, and role-based access control.

![NestJS](https://img.shields.io/badge/NestJS-E0234E?logo=nestjs&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?logo=jsonwebtokens)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?logo=stripe&logoColor=white)

## 🔗 Project Links

- GitHub Repository: https://github.com/lujainIbrahem/E-cmmerce.git  
- API Documentation: https://documenter.getpostman.com/view/44975525/2sB3WpRMEX  

## 🚀 Features

### 🔐 Authentication & Authorization
- User registration and login
- Google OAuth integration
- JWT Access & Refresh Tokens
- Role-Based Access Control (User / Admin)
- Secure password hashing using bcrypt
- OTP verification and password reset

### 🛍 Product Management
- Full CRUD operations for products (Admin only)
- Categories & Subcategories system
- Brand management
- Image upload using Cloudinary
- Product stock & pricing management

### 🛒 Cart System
- Add / update / remove products
- Quantity management
- User-specific cart
- Persistent cart per user

### 📦 Order System
- Create order from cart
- Order status tracking
- Order history per user
- Admin order management

### 🎟 Coupon System
- Create and manage coupons (Admin)
- Apply discount codes
- Expiration & usage validation
- Percentage / fixed discounts support

### 💳 Payment Integration
- Stripe payment gateway integration
- Secure checkout process
- Payment confirmation handling
- Order payment status tracking

## 🔐 Security Features
- JWT Authentication strategy
- Refresh token system
- Token revocation (logout security)
- Helmet security middleware
- CORS protection
- Rate limiting
- Input validation using DTOs

## ☁️ File Handling
- Multer for file uploads
- Cloudinary integration
- Image optimization and storage

## 🧱 Tech Stack

Backend:
- NestJS
- Node.js

Database:
- MongoDB
- Mongoose

Authentication & Security:
- JWT
- bcrypt
- Crypto

Payments:
- Stripe API

Storage:
- Cloudinary
- Multer

## 🗄 Database Models
- User → authentication, roles, profile
- Product → product details, stock, price
- Category / SubCategory → product grouping
- Brand → product branding
- Cart → shopping cart system
- Order → order processing
- Coupon → discount system
- OTP → verification system
- Token Blacklist → revoked sessions

## 🔄 System Flow

Authentication Flow:
User Login → Validate Credentials → Generate Access Token → Generate Refresh Token → Access Protected Routes → Refresh Token when expired

Order Flow:
Add to Cart → Apply Coupon → Create Order → Pay via Stripe → Confirm Order → Update Status

## 🏗 Project Structure

src
├── common
├── module
│   ├── user
│   ├── product
│   ├── cart
│   ├── order
│   ├── category
│   ├── brand
│   ├── coupon
│   └── gateway
├── Db
├── utils
└── main.ts

## 📦 Installation

git clone https://github.com/lujainIbrahem/E-cmmerce.git  
cd E-cmmerce  
npm install  
npm run start:dev  

## ⚙️ Environment Variables

PORT=  
MONGO_URL=  

EMAIL=  
PASS=  

SALT_ROUND=  
ENCRYPT_PHONE=  

SIGNATURE=  

ACCESS_TOKEN_USER=  
ACCESS_TOKEN_ADMIN=  

REFRESH_TOKEN_USER=  
REFRESH_TOKEN_ADMIN=  

CLOUD_NAME=  
API_KEY=  
API_SECRET=  

WEB_CLIENT_ID=  

FRONT_ORIGIN=  

SECRET_STRIPE_KEY=  

## 📌 API Endpoints

Auth:
POST /auth/signUp  
POST /auth/signIn  
POST /auth/logout  
POST /auth/refreshToken  
POST /auth/google  

Users:
GET /users/profile  
PATCH /users/updateProfile  

Products:
POST /product  
GET /product  
GET /product/:id  
PATCH /product/:id  
DELETE /product/:id  

Cart:
POST /cart  
GET /cart  
PATCH /cart  
DELETE /cart  

Orders:
POST /order  
GET /order  
PATCH /order/:id  

Coupons:
POST /coupon  
GET /coupon  

## 🎯 Key Highlights
- Modular NestJS architecture  
- Secure authentication system (JWT + Refresh Token)  
- Role-based authorization  
- Stripe payment integration  
- Cloudinary file storage  
- Clean scalable REST API design  
- Production-ready backend structure  

## 🚀 Future Improvements
- Swagger API documentation  
- Docker containerization  
- Unit & integration testing  
- WebSocket real-time notifications  
- Admin dashboard UI  
- Advanced analytics system  

## 👩‍💻 Author
Lujain Ibrahim  
Backend Developer  
GitHub: https://github.com/lujainIbrahem  

## 📄 License
This project is for educational and portfolio purposes only.