# NatureGrocery - Full Stack Grocery Shopping Web App

**NatureGrocery** is a comprehensive full-stack grocery shopping website built using **React.js**, **Tailwind CSS**, and **MongoDB**. It offers users a smooth, mobile-friendly interface to explore categories, add items to a cart, and place orders with ease.

---

## Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Installation](#-installation)
- [Project Structure](#-project-structure)
- [API & Environment Setup](#-api--environment-setup)
- [Custom Animations](#-custom-animations)
- [Screenshots](#-screenshots)
- [Upcoming Features](#-upcoming-features)
- [Contribution](#-contribution)
- [License](#-license)
- [Contact](#-contact)

---

## Overview

**NatureGrocery** is a modern e-commerce-style grocery web app offering a smooth user experience for both desktop and mobile users. The platform enables:

- Browsing and filtering groceries (Vegetables, Fruits, Snacks, etc.)
- Adding to cart
- Buying instantly (Buy Now)
- Contacting support
- Reading about the brand’s mission
- Animations triggered on scroll or section focus

---

## Key Features

--> User Authentication (JWT with MongoDB)  
--> Add to Cart & Buy Now  
--> Categorized Product Browsing  
--> Scroll & Section-Based Animations  
--> EmailJS-powered Contact Form  
--> Responsive Mobile View  
--> Google Maps Embed for Location  
--> Toast Notifications  
--> Secure Order Placement via API

---

## Tech Stack

### Frontend
--> React.js (Functional Components + Hooks)
--> Tailwind CSS (For fast and flexible UI design)
--> React Icons
--> EmailJS (Contact form submissions)
--> Intersection Observer (for scroll animations)
--> Local Storage (User session handling)

### Backend
--> PyMongo (MongoDB integration)
--> JWT Authentication (Login & Register)
--> RESTful API architecture

### Database
- MongoDB (Atlas Cloud / Local)
- Collections:
  - `users`
  - `orders`
  - `materials` (if AI recommendation is integrated)

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/NatureGrocery.git
cd NatureGrocery
```

### 2. Frontend Setup (React)

```bash
cd client
npm install
```

#### Frontend Dependencies

- `react`
- `react-dom`
- `react-icons`
- `tailwindcss`
- `emailjs-com`
- `postcss`, `autoprefixer`

#### Start Frontend

```bash
npm start
```

### 3. Backend Setup (Flask)

```bash
cd ../backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

#### Backend Libraries

- `PyMongo`
- `python-dotenv`
- `bcrypt`
- `PyJWT`

#### Start Backend

```bash
python app.py
```

---

## Project Structure

```bash
NatureGrocery/
├── client/
│   ├── assets/
│   ├── components/
│   ├── hooks/
│   ├── pages/
│   ├── App.jsx
│   ├── index.css
│   └── tailwind.config.js
├── backend/
│   ├── app.py
│   ├── routes/
│   ├── models/
│   ├── utils/
│   ├── .env
│   └── requirements.txt
├── README.md
└── .gitignore
```

---

## API & Environment Setup

### Sample `.env` file

```bash
MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/NatureGrocery
JWT_SECRET=your_jwt_secret_key
EMAIL_USER=your_email@example.com
EMAIL_PASS=your_email_password
```

### API Endpoints

| Method | Endpoint                     | Description            |
|--------|------------------------------|------------------------|
| POST   | `/api/auth/register`         | Register new user     |
| POST   | `/api/auth/login`            | User login            |
| GET    | `/api/products/:category`    | Get category items    |
| POST   | `/api/orders/create-order`   | Place an order        |

---

## Custom Animations

### `useFlipZoomAnimation` Hook

This hook uses `IntersectionObserver` to detect when the product section or any component comes into view, applying a unique animation like "flip", "zoom", or "bounce".

```js
const observer = new IntersectionObserver(...);
ref.current.classList.add('flip-bounce');
```

> Fully optimized for mobile responsiveness using Tailwind’s responsive utilities.

---

## Screenshots

| Home Screen | Contact Section |
|-------------|------------------|
| `screenshots/home.png` | `screenshots/contact.png` |

---

## Upcoming Features

--> AI Material Recommendation (for building sector)
--> Cart Quantity Editing
--> Admin Dashboard
--> Payment Gateway Integration

---

## Contribution

1. Fork the repo  
2. Create a feature branch  
3. Commit your changes  
4. Push to GitHub  
5. Create a Pull Request  

---

## License

Licensed under the **MIT License**.

---

## Contact

**Santhosh Kumar**  
📧 support@naturegrocery.com  
🌐 [GitHub](https://github.com/Santhosh-The-DeveLoper)
