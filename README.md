# MegaMart — Full-Stack E-Commerce Platform
A fully functional MERN stack e-commerce web application with a customer-facing storefront, an admin dashboard for product and order management, and a RESTful backend API — all deployed and production-ready.

---

## 🌐 Live Demo

| App | URL |
|---|---|
| 🛍️ Frontend (Store) | [mega-mart-sand-seven.vercel.app](https://mega-mart-sand-seven.vercel.app/) |
| ⚙️ Backend API | [megamart-ozkc.onrender.com](https://megamart-ozkc.onrender.com/) |

---

## 🎯 Goal
Build a production-grade, full-stack e-commerce platform with three separate apps:
- **Frontend** — Customer-facing shopping experience with product browsing, cart, and checkout.
- **Admin Panel** — Manage products, categories, and orders from a dedicated dashboard.
- **Backend** — RESTful API serving both frontend and admin with authentication, file uploads, and payment integration.

---

## ⚡ Features

### 🛍️ Frontend (Customer Store)
- Browse and search products with category filters.
- Product detail pages with image galleries and size selection.
- Add to cart, update quantities, and remove items.
- User authentication — register, login, and manage account.
- Checkout flow with order summary and payment integration.
- Order history and tracking for logged-in users.
- Fully responsive design for mobile and desktop.

### 🛠️ Admin Panel
- Secure admin login.
- Add, edit, and delete products with image uploads.
- Manage product categories and inventory.
- View and manage all customer orders.
- Update order status (e.g., Processing → Shipped → Delivered).

### ⚙️ Backend API
- RESTful API built with Express.js.
- JWT-based authentication for users and admins.
- Product CRUD with image storage via Cloudinary.
- Cart and order management endpoints.
- Payment gateway integration (Stripe / Razorpay).
- MongoDB with Mongoose for data modeling.

---

## 🗂️ Project Structure

```
MegaMart/
└── forever-full-stack/
    ├── frontend/       # React customer storefront
    ├── admin/          # React admin dashboard
    └── backend/        # Node.js + Express REST API
```

---

## 💻 Tech Stack

| Layer | Technology |
|---|---|
| **Frontend** | React, React Router, Axios, Tailwind CSS |
| **Admin** | React, React Router, Axios, Tailwind CSS |
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB, Mongoose |
| **Auth** | JSON Web Tokens (JWT), bcrypt |
| **File Storage** | Cloudinary |
| **Payments** | Stripe / Razorpay |
| **Frontend Deploy** | Vercel |
| **Backend Deploy** | Render |

---

## 🚀 Getting Started

### Prerequisites
- Node.js v18+
- npm or yarn
- MongoDB Atlas account (or local MongoDB)
- Cloudinary account
- Stripe or Razorpay account

### 1. Clone the Repository
```bash
git clone https://github.com/Shubham0x1/MegaMart.git
cd MegaMart/forever-full-stack
```

### 2. Set Up the Backend
```bash
cd backend
npm install
```

Create a `.env` file in the `backend/` directory:
```env
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
STRIPE_SECRET_KEY=your_stripe_secret_key
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret
ADMIN_EMAIL=your_admin_email
ADMIN_PASSWORD=your_admin_password
```

Start the backend server:
```bash
npm run server
```
The API will be running at `http://localhost:4000`.

### 3. Set Up the Frontend
```bash
cd ../frontend
npm install
```

Create a `.env` file in the `frontend/` directory:
```env
VITE_BACKEND_URL=http://localhost:4000
```

Start the frontend:
```bash
npm run dev
```
Open `http://localhost:5173` in your browser.

### 4. Set Up the Admin Panel
```bash
cd ../admin
npm install
```

Create a `.env` file in the `admin/` directory:
```env
VITE_BACKEND_URL=http://localhost:4000
```

Start the admin panel:
```bash
npm run dev
```
Open `http://localhost:5174` in your browser.

---

## 🌍 Deployment

### Backend — Render
1. Create a new **Web Service** on [Render](https://render.com).
2. Connect your GitHub repository and set the root directory to `forever-full-stack/backend`.
3. Set the build command: `npm install`
4. Set the start command: `node server.js`
5. Add all environment variables from the `.env` section above.

### Frontend — Vercel
1. Import your GitHub repository on [Vercel](https://vercel.com).
2. Set the root directory to `forever-full-stack/frontend`.
3. Set the framework preset to **Vite**.
4. Add the environment variable `VITE_BACKEND_URL` pointing to your Render backend URL.

### Admin Panel — Vercel
Repeat the same Vercel steps for the `forever-full-stack/admin` directory.

---

## 📡 API Endpoints (Overview)

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/user/register` | Register a new user |
| POST | `/api/user/login` | User login |
| POST | `/api/user/admin` | Admin login |
| GET | `/api/product/list` | Get all products |
| POST | `/api/product/add` | Add a product (admin) |
| DELETE | `/api/product/remove` | Remove a product (admin) |
| GET | `/api/product/single` | Get single product details |
| POST | `/api/cart/add` | Add item to cart |
| POST | `/api/cart/update` | Update cart item |
| POST | `/api/cart/get` | Get user cart |
| POST | `/api/order/place` | Place an order (COD) |
| POST | `/api/order/stripe` | Place an order (Stripe) |
| POST | `/api/order/razorpay` | Place an order (Razorpay) |
| GET | `/api/order/userorders` | Get user's orders |
| GET | `/api/order/list` | Get all orders (admin) |
| POST | `/api/order/status` | Update order status (admin) |

---

## 📄 License
This project is for educational and portfolio purposes.

---

## 👨‍💻 Author
**Shubham Gusain**

GitHub: https://github.com/Shubham0x1

---

## ⭐ Support
If you like this project, consider giving the repository a **star ⭐**.
