## Tech Stack Overview

The **FreshNest** is developed using the **PERN Stack** with **AWS S3** integration for scalable media storage.  
This stack ensures a secure, efficient, and maintainable solution for managing users, products, and orders.

---

| Layer | Technology | Description | Purpose |
|--------|-------------|--------------|-----------|
| **Frontend** | **React.js** | JavaScript library for building responsive user interfaces. | Enables a fast, dynamic, and user-friendly experience for buyers and sellers. |
| **Backend** | **Node.js + Express.js** | Backend runtime and framework for handling APIs and requests. | Manages authentication, authorization, product, and order logic. |
| **Database** | **PostgreSQL** | Relational database for structured data. | Stores users, roles, products, carts, and orders securely and efficiently. |
| **Cloud Storage** | **AWS S3** | Simple Storage Service for storing and retrieving product images. | Enables sellers to upload product images securely using presigned URLs. |
| **Authentication** | **JWT (JSON Web Token)** | Token-based authentication mechanism. | Provides secure login and access control for users and sellers. |
| **Styling** | **Tailwind CSS** | Utility-first CSS framework. | Builds a clean, responsive, and modern UI. |
| **Security** | **Bcrypt.js,CORS** | Libraries for encryption and request protection. | Ensures secure data transmission and protects against common vulnerabilities. |
| **DevOps / Deployment** | **GitHub Actions + AWS EC2** | CI/CD pipeline and cloud instance for hosting. | Automates deployment and ensures scalable cloud hosting. |
| **Environment Config** | **Dotenv** | Environment variable management. | Keeps credentials and configuration secure. |

---

## Summary

The chosen tech stack provides:  
- **Performance:** React + Node ensures smooth frontend-backend communication.  
- **Scalability:** PostgreSQL and AWS EC2 scale easily as traffic grows.  
- **Security:** JWT authentication, bcrypt hashing, and HTTPS for safe data handling.   

This setup ensures a **reliable, secure, and scalable platform** for both buyers and sellers.

---
