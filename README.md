# Ride-Hailing Application Database System


A comprehensive SQL Server database solution for a ride-hailing application, designed to manage driver profiles, user accounts, ride information, payment transactions, and customer reviews.

## 📋 Table of Contents

- [Project Overview](#-project-overview)

- [Database Schema](#-database-schema)

- [Entities and Relationships](#-entities-and-relationships)

- [Features](#-features)

- [SQL Queries](#-sql-queries)

- [Installation & Setup](#-installation--setup)

- [Testing](#-testing)

- [ER Diagram](#-er-diagram)

- [Normalization](#-normalization)

- [Technical Documentation](#-technical-documentation)

---

## 🎯 Project Overview

This project was developed as part of **CSE4005 - Database Design and Development** module for Infor Pvt Ltd, a leading IT company planning to develop a new ride-hailing application. The database system handles large volumes of data related to driver profiles, user accounts, ride information, and payment transactions.



## 🗃️ Database Schema

The database consists of the following main tables:

- **User** - Stores customer registration information

- **Driver** - Manages driver profiles and vehicle details

- **Ride** - Tracks ride bookings and details

- **Payment** - Handles payment transactions

- **Review** - Stores customer feedback and ratings

- **VehicleType** - Reference table for vehicle types

- **VehicleColour** - Reference table for vehicle colors

- **PaymentTypes** - Reference table for payment methods



## 🔗 Entities and Relationships

### Key Relationships:

- **User → Ride** (One-to-Many): A user can book multiple rides

- **Driver → Ride** (One-to-Many): A driver can handle multiple rides (one at a time)

- **Ride → Payment** (One-to-One): Each ride has one payment

- **Ride → Review** (One-to-Many): A ride can have multiple reviews

- **Driver → VehicleType/VehicleColour** (Many-to-One): Drivers are associated with vehicle types and colors



## ✨ Features

- **User Management**: Complete user registration and profile management

- **Driver Management**: Driver registration with vehicle details

- **Ride Booking**: Comprehensive ride tracking with pickup/dropoff locations

- **Payment Processing**: Multiple payment methods supported

- **Review System**: Star ratings and feedback mechanism

- **Data Integrity**: Foreign key constraints and validation rules

- **Query Optimization**: Efficient SQL queries for reporting



## 📊 SQL Queries

The database includes essential queries for:

1. **List all driver details**

2. **Retrieve reviews for a specific driver**

3. **View ride history for a specific user**

4. **Filter rides by date range for a particular driver**

5. **Calculate total revenue per driver**



## 🔧 Installation & Setup

**Prerequisites:**

* Microsoft SQL Server (2016 or later)

* SQL Server Management Studio (SSMS)


### Installation Steps:

**Create Database:**
```
sql

CREATE DATABASE [CSE 4005 Prabath];
```

**Execute SQL Script:**

* Open SSMS

* Connect to your SQL Server instance

* Open the provided script.sql file

* Execute the entire script


### Verify Installation:

* Check that all tables are created successfully

* Verify that sample data is inserted (15 records per table)

* Confirm foreign key relationships are established

## 🧪 Testing

Comprehensive testing conducted including:

### Test Types:

**1. Unit Testing:** Individual component validation

**2. Integration Testing:** Cross-table relationship verification

**3. Functional Testing:** Business logic validation

**4. Constraint Testing:** Foreign key and data integrity checks

## Sample Test Cases:

* Insert valid driver data

* Prevent rides with non-existing drivers

* Validate payment references

* Check case sensitivity on usernames

* Verify date range filtering

## 📐 ER Diagram

### The Entity Relationship Diagram illustrates:

* All main entities and their attributes

* Primary keys (underlined) and foreign key relationships

* Relationship types (one-to-many, one-to-one)

* Attribute data types and constraints

## 📈 Normalization

The database is normalized up to 3NF (Third Normal Form):

### Normalization Process:

**1NF:** All attributes contain atomic values

**2NF:** No partial dependencies (all non-prime attributes fully dependent on primary keys)

**3NF:** No transitive dependencies (all attributes dependent only on the primary key)

## 📚 Technical Documentation

### Database Specifications:

* Database Name: CSE 4005 Prabath

* SQL Version: Compatible with SQL Server 2016+

* Character Set: Default database collation

* Security: Standard SQL Server authentication

### Key Constraints:

* Primary keys on all main tables

* Foreign key constraints for referential integrity

* Appropriate data types for all attributes

* Identity specification for auto-incrementing keys

---

**Developer:** Prabath Jayasuriya

**Module:** CSE4005 - Database Design and Development

**Academic Year:** 2025, Semester 2

