# 🛒 E-Commerce Backend API (NestJS)

A scalable and secure **E-Commerce Backend System** built with **NestJS**, **MongoDB**, and modern backend architecture principles.  
The system is designed using a **modular architecture** following NestJS best practices with separation of concerns across modules, services, controllers, and shared common layer.

It supports full e-commerce workflow including authentication, products, cart, orders, coupons, payments, and real-time features.

![NestJS](https://img.shields.io/badge/NestJS-E0234E?logo=nestjs&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?logo=jsonwebtokens)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?logo=stripe&logoColor=white)

## 🔗 Project Links
- GitHub Repository: https://github.com/lujainIbrahem/E-cmmerce.git  
- API Documentation: https://documenter.getpostman.com/view/44975525/2sB3WpRMEX  

---

## 🚀 Features

### 🔐 Authentication Module
- User registration & login
- Google OAuth integration
- JWT Access & Refresh tokens
- Role-Based Access Control (User / Admin)
- OTP verification system
- Password reset & update password
- Token revocation (logout system)

---

### 👤 User Module
- Profile management
- Update user data
- Secure user session handling

---

### 🛍 Product Module
- Full CRUD operations (Admin)
- Product image upload (Cloudinary)
- Stock & price management
- Product listing & details
- Category & SubCategory relation

---

### 🗂 Category & Brand Modules
- Category management
- SubCategory mapping
- Brand management system

---

### 🛒 Cart Module
- Add / update / remove items
- Quantity control
- User-specific cart

---

### 📦 Order Module
- Create order from cart
- Order status tracking
- Order history per user
- Admin order management

---

### 🎟 Coupon Module
- Create & validate coupons
- Discount system (percentage / fixed)
- Expiration handling

---

### 💳 Payment Integration
- Stripe checkout integration
- Payment confirmation flow
- Secure transaction handling

---

### 🔌 Gateway Module
- WebSocket gateway support (real-time structure ready)

---

## 🔐 Security Implementation (Common Layer)
- JWT authentication guard
- Authorization guard (RBAC)
- Helmet security
- CORS configuration
- Rate limiting
- DTO validation
- Token encryption & signature system

---

## ☁️ File Upload System (Utils)
- Multer local & cloud storage
- Cloudinary integration
- File validation middleware

---

## 🧱 Tech Stack

**Backend Framework**
- NestJS

**Runtime**
- Node.js

**Database**
- MongoDB (Mongoose)

**Auth & Security**
- JWT
- bcrypt
- Crypto

**Payments**
- Stripe API

**Storage**
- Cloudinary
- Multer

---

## 🗄 Database Layer (Db Module)

- User Model
- Product Model
- Category Model
- SubCategory Model
- Brand Model
- Cart Model
- Order Model
- Coupon Model
- OTP Model

---

## 🔄 System Architecture Flow

### Authentication Flow
User → Auth Module → Validate Credentials → Generate JWT Tokens → Guards → Protected Routes

### Order Flow
Cart → Coupon Validation → Order Creation → Stripe Payment → Order Confirmation → Status Update

---

## 🏗 Project Structure (NestJS)

src
├── common
│   ├── decorators
│   ├── guards
│   ├── middleware
│   ├── enums
│   ├── interfaces
│   └── services
├── module
│   ├── auth
│   ├── user
│   ├── product
│   ├── cart
│   ├── order
│   ├── category
│   ├── subCategory
│   ├── brand
│   ├── coupon
│   └── gateway
├── Db
│   ├── models
│   └── repositories
├── utils
│   ├── multer
│   ├── hash
│   └── email
└── main.ts

---

## 📦 Installation

git clone https://github.com/lujainIbrahem/E-cmmerce.git  
cd E-cmmerce  
npm install  
npm run start:dev  

---

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

---

## 📌 API Endpoints

### Auth Module
POST /auth/signUp  
POST /auth/signIn  
POST /auth/logout  
POST /auth/refreshToken  
POST /auth/google  

### User Module
GET /users/profile  
PATCH /users/updateProfile  

### Product Module
POST /product  
GET /product  
GET /product/:id  
PATCH /product/:id  
DELETE /product/:id  

### Cart Module
POST /cart  
GET /cart  
PATCH /cart  
DELETE /cart  

### Order Module
POST /order  
GET /order  
PATCH /order/:id  

### Coupon Module
POST /coupon  
GET /coupon  

---

## 🎯 Key Highlights
- Real NestJS modular architecture  
- Clean separation of modules (auth/product/order/etc)  
- Secure JWT + refresh token system  
- Scalable DB design with repositories layer  
- Cloudinary + Multer integration  
- Stripe payment gateway  
- Production-level backend structure  

---

## 🚀 Future Improvements
- Swagger API documentation  
- Docker support  
- Unit & integration testing  
- WebSocket real-time updates  
- Admin dashboard UI  
- Caching with Redis  

---

## 👩‍💻 Author
Lujain Ibrahim  
Backend Developer  
GitHub: https://github.com/lujainIbrahem  

---

## 📄 License
This project is for educational and portfolio purposes only.