
# 📦 GadgetBox — Electronics E-commerce Platform

**GadgetBox** is a fully functional e-commerce web application for electronics, developed using **Django + Django REST Framework** (Backend) and **ReactJS** (Frontend). It offers a modern UI, API-driven architecture, and modular code structure optimized for scalability and clarity.

---

## 🚀 Features Overview

### 🛍️ Product Management
- Create, update, and delete electronic products
- Categorization and filtering of gadgets
- Product detail view with specs, image, price, and availability
- Dynamic product listing through React frontend

### 🧾 Orders & Cart
- Add products to cart
- Checkout flow
- Order creation and confirmation
- REST API endpoints for cart & order management

### 👤 User Management
- User registration, login, logout
- Authentication using token/session
- User profile view & edit
- Admin panel for user and product control

### 🌐 API Layer (DRF-based)
- `base/urls/product_urls.py` — Product CRUD operations  
- `base/urls/order_urls.py` — Cart & order operations  
- `base/urls/user_urls.py` — User authentication & profile APIs  
- Organized `serializers.py` and `views.py` for maintainability

### 📦 Admin Panel (Django)
- Manage users, orders, and inventory
- Admin permissions and staff-only access
- Visual management interface

### 💅 Frontend (React)
- Modern, responsive SPA interface
- Routes: `/products`, `/cart`, `/login`, `/signup`, `/profile`, `/checkout`
- API integration via Axios
- React Context / Redux support for state management
- Styled with Bootstrap or Tailwind (if added)

---

## 🛠️ Tech Stack

| Layer     | Tech                           |
|-----------|--------------------------------|
| Frontend  | ReactJS, React Router DOM, Axios |
| Backend   | Django, Django REST Framework  |
| Database  | SQLite (default), PostgreSQL-ready |
| Auth      | Django Auth / Token-based Auth |
| Styling   | Bootstrap / Tailwind CSS       |
| API Design| RESTful, versioned endpoints   |
| Dev Tools | VS Code, GitHub, Git, yarn/npm |

---

## 📁 Folder Structure

```
project-ecommerce2.0/
│
├── backend/
│   ├── base/
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── views.py
│   │   ├── urls/
│   │   │   ├── product_urls.py
│   │   │   ├── order_urls.py
│   │   │   └── user_urls.py
│   ├── static/
│   ├── db.sqlite3
│   └── manage.py
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── App.js
│   │   └── index.js
│   ├── package.json
│   └── yarn.lock
│
├── myenv/
└── README.md
```

---

## ⚙️ Setup Instructions

### 🔧 Backend (Django)

```bash
cd backend
python -m venv myenv
myenv\Scripts\activate   # Windows
pip install -r requirements.txt

python manage.py makemigrations
python manage.py migrate
python manage.py runserver
```

Runs on: `http://127.0.0.1:8000`

---

### ⚛️ Frontend (React)

```bash
cd frontend
npm install
npm start
```

Runs on: `http://localhost:3000`

---

## 📡 API Endpoints (Sample)

| Endpoint                    | Method | Description           |
|----------------------------|--------|-----------------------|
| `/api/products/`           | GET    | List all products     |
| `/api/products/<id>/`      | GET    | Product details       |
| `/api/users/register/`     | POST   | User registration     |
| `/api/users/login/`        | POST   | User login            |
| `/api/orders/`             | POST   | Create order          |
| `/api/orders/myorders/`    | GET    | Get user's orders     |

---

## 🔒 Authentication

- Uses Django's built-in user model
- API endpoints protected via `@permission_classes`
- JWT or Session-based auth (based on setup)

---

## 📈 Future Enhancements (Ideas)

- Payment integration (Razorpay/Stripe)
- Wishlist & product reviews
- Multi-vendor support
- Admin dashboard with analytics
- Docker + CI/CD deployment

---

## 👨‍💻 Author

**Bijoy Laxmi Biswas (@techtrotter)**  
Engineer | Techie Traveler | Django & React Developer  
🔗 [LinkedIn](https://www.linkedin.com/in/bijoy-laxmi-biswas-cse07/)
