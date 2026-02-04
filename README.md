Ottimo lavoro con la documentazione, Luca! Hai strutturato il progetto in modo molto professionale, coprendo tutti i pilastri di una progettazione database fatta a dovere: dal concettuale alla gestione delle integrità.

Ho aggiornato la sezione **Technologies Used** per specificare l'uso di **PostgreSQL**, mantenendo lo stile pulito e tecnico che hai impostato.

---

# 🍕 Cibora Food Delivery Database Project

## 📝 Overview

**Cibora** is a comprehensive database system designed for an innovative food delivery platform. Developed for the *Database Project course of Università degli Studi di Torino*, the system manages interactions between restaurants, customers, riders, and complex ordering processes.

## ✨ Main Features

* **User Management:** Registration, premium subscriptions, electronic wallets ("Borsellino"), and discount codes.
* **Restaurant Ecosystem:** Detailed profiles, categories, and "Top Partner" reward systems.
* **Menu & Catalog:** Multiple menus, categorized sections, allergen tracking, and dynamic pricing.
* **Logistics & Riders:** Real-time tracking (GPS), vehicle classification, and distance-based assignment.
* **Customer Support:** Integrated chat tools, formal complaints (Reclamo), and review system.

## 🛠️ Technologies Used

* **Database Management System (DBMS):** **PostgreSQL** (specifically chosen for its robust support of complex constraints and data integrity).
* **Modeling:** Entity-Relationship (E-R) Diagramming.
* **Languages:** DDL (Data Definition Language) and DML (Data Manipulation Language) using Standard SQL.

## 🗄️ Database Design Highlights

### 🧠 Conceptual Schema (E-R)

The initial design includes complex entities such as **Utente**, **Rider**, **Ristorante**, and **Ordine**, utilizing generalizations for riders and specialized restaurant tiers.

### 🔄 Restructuring & Optimization

* **Redundancy Analysis:** Evaluation of derived attributes (e.g., "Order Total") to balance storage vs. performance.
* **Generalization Removal:** Merging rider types into a single table with a "Mezzo" attribute.
* **Identifier Selection:** Transitioning to simplified unique codes (e.g., `CodiceRistorante`) for better indexing.

### 🛡️ Integrity Rules

* **Order States:** Strict transitions from *In Processing* to *Delivered*.
* **Delivery Logic:** E-bikes prioritized for routes exceeding 10km.
* **Safety Constraints:** Prevention of deletion for active users/restaurants during delivery.

## 🚀 Implementation & Testing

1. **DDL:** Tables created in **PostgreSQL** with strict `CHECK` constraints (e.g., ratings between 1-5).
2. **DML:** Realistic sample data for restaurants, users, and delivery scenarios.
3. **Constraint Testing:** Verification of `ON DELETE CASCADE` and `SET NULL` behaviors.

---

> **🎓 Educational Purpose**
> This project was developed by **Luca Robustelli** as an academic requirement for the University of Turin. It is a theoretical design meant to demonstrate database architectural principles on **PostgreSQL**.

---

Ti serve aiuto per scrivere qualche **Trigger** specifico in PL/pgSQL per gestire la logica dei chilometri o gli stati degli ordini?
