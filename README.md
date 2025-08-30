
# **CSSPMS.GRAMMAR Online Academy Platform**

Welcome to the **CSSPMS.GRAMMAR Online Academy Platform**, a dynamic educational platform designed to deliver high-quality courses to students, allowing them to browse, purchase, and enroll in educational content. The platform is built using a **headless architecture** with **Next.js** for the frontend and a **Python backend** (Django/FastAPI) to handle APIs and business logic.

## **Table of Contents**

1. [Project Overview](#project-overview)
2. [Tech Stack](#tech-stack)
3. [Features](#features)
4. [User Roles & Pages](#user-roles-and-pages)
5. [Setup & Installation](#setup-and-installation)
6. [Configuration](#configuration)
7. [Video Hosting & Storage](#video-hosting-and-storage)
8. [Authentication](#authentication)
9. [Payment Integration](#payment-integration)
10. [Security Best Practices](#security-best-practices)
11. [SEO & Performance Optimization](#seo-and-performance-optimization)
12. [Contributions](#contributions)
13. [License](#license)

## **Project Overview**

The **CSSPMS.GRAMMAR** platform is a modern, full-stack educational website that uses a **headless CMS architecture**, ensuring separation between the **frontend** and **backend** for a more scalable and maintainable system. The platform is designed to offer **online courses**, manage users, payments, and provide an easy-to-use admin panel for content management.

---

## **Tech Stack**

* **Frontend**:

  * **Next.js (React)** – for dynamic and server-side rendered (SSR) pages.
  * **Tailwind CSS** – for responsive and clean styling.
  * **SWR** – for data fetching from APIs.

* **Backend**:

  * **Django** (with **Django REST Framework**) or **FastAPI** – for building robust REST APIs.
  * **PostgreSQL** or **MongoDB** – for relational/non-relational database management.

* **Authentication**:

  * **Google OAuth2** via **NextAuth.js**.

* **Video Storage**:

  * **AWS S3** or **Google Cloud Storage** for video storage with signed URLs for security.

* **Payment**:

  * **Razorpay** (for integrated payment gateway) or **Manual Payment** (JazzCash, EasyPaisa).

* **Hosting**:

  * **Vercel/Netlify** for hosting the **Next.js** frontend.
  * **Heroku/AWS** for hosting the **Django/FastAPI** backend.

---

## **Features**

### **1. Student (Learner) Features**:

* **Browse Courses**: Display a course catalog with details, price, description, and thumbnail.
* **Course Detail Page**: View detailed course information, including syllabus, pricing, and video previews.
* **Enroll & Purchase**: Add courses to cart, make payments via Razorpay or offline payment methods.
* **My Courses Dashboard**: View and manage enrolled courses.
* **Course Content**: Access lecture videos securely hosted on AWS S3 or Google Cloud Storage.
* **Account Management**: Update profile, change password, view order history.

### **2. Admin Features**:

* **Create/Edit Courses**: Admins can create, edit, and manage courses, including titles, descriptions, pricing, images, and tags.
* **Add Lectures/Videos**: Admins can add videos to each course using URLs from secure video storage.
* **User Management**: Admins can view, manage, and remove users.
* **Sales Analytics**: View revenue and sales data through integrated analytics.

### **3. Public Features**:

* **Public Pages**: Home page, About Us, Contact, and course previews for unauthenticated users.
* **Sign Up & Log In**: Option for users to sign up and log in via email or Google OAuth.

---

## **User Roles & Pages**

### **1. Students/Users**:

* **Home**: Browse available courses.
* **Course Detail**: Information about each course.
* **My Courses**: List of enrolled courses.
* **Profile**: User account settings and personal details.
* **Order History**: View past orders and payment statuses.
* **Contact/Support**: A page for user inquiries.

### **2. Admins**:

* **Admin Dashboard**: Manage courses, users, and content.
* **Course Management**: Create, edit, and manage courses and lectures.
* **User Management**: Approve or reject new registrations, manage roles, and delete users.
* **Sales & Analytics**: View sales data and platform performance.

---

## **Setup & Installation**

### **1. Clone the Repository**:

```bash
git clone https://github.com/your-repository-name.git
cd your-repository-name
```

### **2. Install Dependencies**:

For the frontend:

```bash
cd frontend
npm install
```

For the backend:

```bash
cd backend
pip install -r requirements.txt
```

### **3. Configure the Database**:

* Set up **PostgreSQL** or **MongoDB** based on the database choice.
* Create a `.env` file for database credentials and API keys.

### **4. Run Development Servers**:

* For **frontend** (Next.js):

```bash
npm run dev
```

* For **backend** (Django):

```bash
python manage.py runserver
```

---

## **Configuration**

* **Frontend**:

  * In the `.env` file, set up the **API URL** for fetching data from the backend.
  * Set up **Google OAuth2** keys in the frontend.

* **Backend**:

  * Configure **Google OAuth2** integration.
  * Set up **payment gateway (Razorpay)** credentials.

---

## **Video Hosting & Storage**

* **Cloud Video Hosting**:

  * Use **AWS S3** or **Google Cloud Storage** for secure video hosting.
  * Set up **signed URLs** for secure video streaming, ensuring only authorized users can view the content.

---

## **Authentication**

* **Google OAuth2**: Users can sign in using their Google account.
* **JWT Tokens**: After successful login, the backend issues a **JWT token** for secure session management.

---

## **Payment Integration**

* **Razorpay**: Integrate Razorpay for online payment processing.

  * On successful payment, the backend updates the user’s enrollment status and provides access to the purchased course content.

---

## **Security Best Practices**

* **SSL**: Use HTTPS for secure communication between the frontend and backend.
* **Password Hashing**: Ensure all passwords are securely hashed using **bcrypt**.
* **Data Validation**: Use Django’s built-in validation for input sanitization.
* **Video Protection**: Use **signed URLs** or DRM to prevent unauthorized access to course videos.

---

## **SEO & Performance Optimization**

* **SEO**: Use **Next.js SSR** (server-side rendering) for SEO-friendly pages.
* **Lazy Loading**: Implement lazy loading for images and videos to improve page load times.
* **Responsive Design**: Ensure that all pages are fully responsive across mobile, tablet, and desktop devices.

---

## **Contributions**

Feel free to fork the repository, open issues, or create pull requests. Contributions are always welcome!

---

## **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

