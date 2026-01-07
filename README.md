# 🍕 Cibora Food Delivery Database Project

## 📝 Overview

**Cibora** is a comprehensive database system designed for an innovative food delivery platform. Developed by **Luca Robustelli** (Me) for the *Database Project course of Università degli Studi di Torino* , the system manages interactions between restaurants, customers, riders, and complex ordering processes.

The project covers the entire lifecycle of database design, from conceptual modeling to SQL implementation.

## ✨ Main Features

* **User Management:** Handles registration, premium subscriptions, electronic wallets ("Borsellino"), and discount code collection.


* **Restaurant Ecosystem:** Manages detailed restaurant profiles, categories, and a "Top Partner" reward system for high-performing vendors.


* **Menu & Catalog:** Supports multiple menus per restaurant, categorized sections, allergen tracking, and dynamic pricing with discounts.


* **Logistics & Riders:** Real-time rider tracking (GPS), vehicle classification (Bicycles, E-bikes, Scooters), and optimized distance-based delivery assignment.


* **Customer Support:** Integrated chat tools for users, restaurants, and riders, along with a formal complaint (Reclamo) and review system.



## 🛠️ Technologies Used

* **Database Engine:** PostgreSQL / Standard SQL.


* **Modeling:** Entity-Relationship (E-R) Diagramming.


* **Languages:** DDL (Data Definition Language) and DML (Data Manipulation Language).



## 🗄️ Database Design Highlights

### 🧠 Conceptual Schema (E-R)

The initial design includes complex entities such as **Utente**, **Rider**, **Ristorante**, and **Ordine**. It utilizes generalizations for different types of riders (based on vehicle) and specialized restaurant tiers.

### 🔄 Restructuring & Optimization

To ensure maximum performance, the schema underwent several optimizations:

* **Redundancy Analysis:** Evaluation of derived attributes like "Order Total" and "Restaurant Rating" to balance storage vs. calculation speed.


* **Generalization Removal:** Merging rider types into a single table with a "Mezzo" attribute to simplify queries.


* **Identifier Selection:** Transitioning from composite primary keys to simplified unique codes (e.g., `CodiceRistorante`) for better indexing.



### 🛡️ Integrity Rules

* **Order States:** Orders transition strictly through *In Processing, Assigned, In Delivery, Delivered, or Not Delivered*.


* **Delivery Logic:** E-bikes are prioritized for routes exceeding 10km.


* **Safety Constraints:** Users or restaurants cannot be deleted if they have active "In Delivery" orders.



## 🚀 Implementation & Testing

The project includes a complete set of SQL commands:

1. **DDL:** Tables created with strict constraints (e.g., `CHECK` constraints for ratings between 1 and 5).


2. **DML:** Sample data for 3 restaurants, multiple users, and various delivery scenarios.


3. **Constraint Testing:** Verification of `ON DELETE CASCADE` and `SET NULL` behaviors when users or allergens are removed.



---

> **🎓 Educational Purpose**
> This project was developed by **Luca Robustelli** as an academic requirement for the University of Turin. It is a theoretical design meant to demonstrate database architectural principles.
> 
> 

