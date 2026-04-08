# 📊 Database Design Projects

This repository contains ER diagram designs for two real-world systems:

1. 🛍️ Instagram Thrift Store Management System  
2. 🏥 Clinic Management System  

These designs focus on **real-world scalability, normalization, and practical use cases**.

---

# 🛍️ Instagram Thrift Store Database

## 📌 Overview
This system is designed for a small Instagram-based business that sells:
- Thrifted (unique, single-piece) items  
- Handmade (multi-unit) products  

Initially managed via DMs and WhatsApp, this design helps scale operations by structuring:
- Inventory
- Orders
- Customers
- Payments
- Shipping

---

## 🧩 Key Features

- Supports **both unique and reusable inventory**
- Tracks **product variants** (size, color, condition)
- Handles **multiple orders per customer**
- Supports **multiple items per order**
- Tracks **payment and shipping status**

---

## 🏗️ Entities

- **Customer**
- **Order**
- **Product**
- **Variant (Inventory)**
- **OrderItem (Junction Table)**
- **Payment**
- **Shipment**

---

## 🔗 Relationships

- One customer → many orders  
- One order → many order items  
- One product → many variants  
- Many-to-many between orders and products (via OrderItem)  
- One order → one payment  
- One order → one shipment  

---

## 💡 Special Design Considerations

- Thrift items → `stock_quantity = 1`  
- Handmade items → `stock_quantity > 1`  
- Condition attribute added for thrift products  
- Price stored in OrderItem to preserve historical pricing  

---

## 📷 ER Diagram

> Add your image or diagram link here  




---

# 🏥 Clinic Management System Database

## 📌 Overview

This system models a clinic where:
- Patients book appointments
- Doctors diagnose and prescribe treatments
- Staff manages records, billing, and schedules

---

## 🧩 Key Features

- Patient record management  
- Appointment scheduling  
- Doctor specialization tracking  
- Prescription and treatment records  
- Billing and payment tracking  

---

## 🏗️ Entities

- **Patient**
- **Doctor**
- **Appointment**
- **Prescription**
- **Medicine**
- **Billing / Payment**
- **Staff (optional)**

---

## 🔗 Relationships

- One patient → many appointments  
- One doctor → many appointments  
- One appointment → one prescription  
- One prescription → many medicines  
- One appointment → one billing record  

---

## 💡 Special Design Considerations

- Appointment acts as a **central entity**  
- Prescriptions linked to appointments (not directly to patients)  
- Supports **doctor specialization**  
- Billing separated for better financial tracking  

---

## 📷 ER Diagram

> Add your image or diagram link here  