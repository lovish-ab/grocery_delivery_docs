
## 1. Introduction
This section describes all possible **use cases** for the Grocery Delivery Website, built using the **PERN stack (PostgreSQL, Express.js, React.js, Node.js)** with **AWS** for image storage.  
The document outlines how both buyers and sellers will interact with the system once it is developed.

---

## 2. Actors

| Actor | Description |
|--------|--------------|
| **Buyer** | Registered customer who can browse, add to cart, and purchase groceries. |
| **Seller** | Vendor who can add, edit, and manage products and orders. |
| **System** | The web application that processes user actions, stores data, and handles requests through APIs. |

---

## 3. Use Case Summary

| Use Case | Actor | Description |
|-----------|--------|-------------|
| Register / Login | Buyer, Seller | Authenticate users using email and password. |
| Browse Products | Buyer, Guest | View, search, and filter grocery products. |
| Add to Cart | Buyer | Add grocery items to the shopping cart. |
| Checkout | Buyer | Confirm cart items and place an order. |
| View Orders | Buyer | Check past and ongoing orders with delivery status. |
| Add Product | Seller | Add a new product with details and upload image to AWS. |
| Manage Orders | Seller | View, process, and update customer orders. |
| Logout | Buyer, Seller | End the active session securely. |

---

## 4. Detailed Use Cases

### UC1: Register / Login
**Actor:** Buyer / Seller  
**Description:** Allows users to create accounts or log into the system securely.  
**Flow:**

1. User enters email and password.
2. The system verifies credentials in **PostgreSQL**.
3. If valid, a **JWT token** is generated for session management.
4. User is redirected to the respective dashboard (Buyer / Seller).

**Alternate Flow:**
- Invalid credentials → Error message displayed.

**Post-condition:** User session becomes active and authenticated.

---

### UC2: Browse Products
**Actor:** Buyer / Guest  
**Description:** Displays all available grocery items and allows searching or filtering.  
**Flow:**

1. User opens the homepage.
2. The system fetches product data from the **PostgreSQL** database.
3. Products are displayed by category or popularity.
4. Clicking on a product opens a detailed view.

**Post-condition:** Products displayed successfully.

---

### UC3: Add to Cart
**Actor:** Buyer  
**Description:** Allows users to select items to purchase.  
**Flow:**

1. User clicks "Add to Cart" on a product.
2. Product details are temporarily stored (in local storage or user session).
3. Cart icon updates with the new count.
4. Cart items are saved in the database for logged-in users.

**Alternate Flow:**  
- If a product is out of stock → Display “Out of Stock” message.

**Post-condition:** Selected items are visible in the user’s cart.

---

### UC4: Checkout
**Actor:** Buyer  
**Description:** Finalizes purchase and creates an order record.  
**Flow:**

1. User reviews cart and clicks “Checkout.”
2. System validates cart data and stock availability.
3. Buyer enters shipping address and simulated payment details.
4. Order details are stored in **PostgreSQL**.

**Post-condition:** Order successfully created and assigned a unique order ID.

---

### UC5: View Orders
**Actor:** Buyer  
**Description:** Enables buyers to track all their orders.  
**Flow:**

1. Buyer navigates to “My Orders.”
2. System retrieves order list and status from the database.

**Post-condition:** Buyer can view both past and ongoing orders.

---

### UC6: Add Product
**Actor:** Seller  
**Description:** Allows sellers to add grocery items for customers to view and purchase.  
**Flow:**

1. Seller logs into their dashboard.  
2. Fills out product details (name, price, category,etc).  
3. Uploads an image via a **presigned URL** to **AWS S3**.  
4. The image URL and product data are stored in **PostgreSQL**.  

**Post-condition:** Product becomes visible to all buyers.

---

### UC7: Manage Orders
**Actor:** Seller  
**Description:** Allows sellers to manage customer orders and update their status.  
**Flow:**

1. Seller opens the “Orders” section on the dashboard.  
2. System displays orders assigned to that seller.
3. Buyer receives the updated status in their account view.

**Post-condition:** Orders are updated and synchronized for both users.

---

### UC8: Logout
**Actor:** Buyer / Seller  
**Description:** Ends the active session for a logged-in user.  
**Flow:**

1. User clicks the “Logout” button.  
2. JWT token is removed or invalidated on the client side.  
3. User is redirected to the login page.

**Post-condition:** User session ends securely.

---

## 5. Summary

The use cases described above outline how both buyers and sellers will interact with the **Grocery Delivery Website** once it is developed.  
All business operations — from browsing groceries to managing orders — will be handled through a secure and efficient **PERN stack** system with **AWS** for scalable media storage.

