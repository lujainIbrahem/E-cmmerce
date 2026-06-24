# 🛒 E-Commerce Backend API

A scalable and secure **E-Commerce Backend System** built with **NestJS**, **MongoDB**, and modern backend best practices. The system supports full e-commerce workflow including authentication, products, cart, orders, coupons, payments, and role-based access control.

![NestJS](https://img.shields.io/badge/NestJS-E0234E?logo=nestjs&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white) ![JWT](https://img.shields.io/badge/JWT-black?logo=jsonwebtokens) ![Stripe](https://img.shields.io/badge/Stripe-635BFF?logo=stripe&logoColor=white)

## 🔗 Project Links
- Repository: https://github.com/lujainIbrahem/E-cmmerce.git  
- API Documentation: https://documenter.getpostman.com/view/44975525/2sB3WpRMEX  

## ⚙️ Features

### Authentication & Authorization
- User registration and login  
- Google OAuth integration  
- JWT Access & Refresh tokens  
- Role-Based Access Control (User / Admin)  
- Secure password hashing (bcrypt)  
- OTP verification & password reset  

### Product System
- CRUD operations for products (Admin)  
- Categories & Subcategories  
- Brand management  
- Image upload via Cloudinary  

### Cart System
- Add / update / remove items  
- Quantity management  
- User-specific cart  

### Order System
- Create orders from cart  
- Order status tracking  
- Order history per user  
- Admin order management  

### Coupons System
- Create & manage coupons  
- Apply discount codes  
- Expiration & usage validation  

### Payments
- Stripe payment integration  
- Secure checkout flow  
- Payment confirmation handling  

## 🔐 Security Implementation
- JWT authentication strategy  
- Token revocation (logout security)  
- Helmet middleware protection  
- CORS configuration  
- Rate limiting protection  
- Input validation using DTOs  

## ☁️ File Storage
- Multer for file handling  
- Cloudinary integration  
- Image upload optimization  

## 🧱 Tech Stack

Backend:
- NestJS
- Node.js

Database:
- MongoDB
- Mongoose

Auth & Security:
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
- Product → product data, pricing, stock  
- Category / SubCategory → product organization  
- Brand → product branding  
- Cart → shopping cart  
- Order → order processing  
- Coupon → discounts  
- OTP → verification codes  
- Token blacklist → revoked sessions  

## 🔄 System Flow

Authentication Flow: User Login → Validate Credentials → Generate Tokens → Access Protected Routes → Refresh Token when expired  

Order Flow: Add to Cart → Apply Coupon → Create Order → Pay via Stripe → Confirm Order → Update Status  

## 🏗 Project Structure
src/ ├── common/ ├── module/ │ ├── user/ │ ├── product/ │ ├── cart/ │ ├── order/ │ ├── category/ │ ├── brand/ │ ├── coupon/ │ └── gateway/ ├── Db/ ├── utils/ └── main.ts  

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
- Secure authentication system  
- Scalable backend design  
- Stripe payment integration  
- Cloudinary file storage  
- Clean REST API design  

## 🚀 Future Improvements
- Swagger documentation  
- Docker support  
- Unit & integration testing  
- WebSocket real-time updates  
- Admin dashboard UI  

## 👩‍💻 Author
Lujain Ibrahim  
Backend Developer  
GitHub: https://github.com/lujainIbrahem  

## 📄 License
This project is intended for educational and portfolio purposes.