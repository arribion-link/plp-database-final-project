# Clinic Booking System - MySQL Database Schema

Description
This project provides a complete MySQL database schema for a **Clinic Booking System. The system is designed to manage patients, doctors, clinic staff (via roles), medical services, appointments, doctor availability, medical records, prescriptions, and basic billing.

The schema is structured using relational database principles, emphasizing normalization to reduce redundancy and improve data integrity. It includes various constraints such as Primary Keys, Foreign Keys, `NOT NULL`, `UNIQUE`, and `CHECK` constraints.

 Key Features of the Schema:
User Management: Handles different user roles (Admin, Doctor, Patient, Receptionist) with separate tables for `UserAccounts` and `Roles`.
Patient Management: Stores patient demographics, contact information, and medical history summary.
Doctor Management: Stores doctor profiles, specialties, and links to user accounts for login.
Appointment Booking: Core functionality allowing patients to book appointments with specific doctors for particular services at given clinic locations.
Doctor Availability: A simplified model for managing recurring weekly availability of doctors.
Medical Services: Defines the services offered by the clinic, including duration and price.
Medical Records & Prescriptions: Allows for storing visit details, diagnoses, treatment plans, and prescribed medications.
Billing & Payments: Basic invoicing for appointments and tracking payments.
Multi-Location Support: Designed to support clinics with multiple physical locations.
Referential Integrity:** Enforced through foreign key constraints.

# How to Run/Setup the Project (Import SQL)

To use this schema, you need a MySQL server instance.

Prerequisites:
MySQL Server installed (Version 8.0+ is recommended for full `CHECK` constraint support, though it should largely work on older 5.7+ versions).
A MySQL client tool such as:
 MySQL Workbench (GUI)
   DBeaver (GUI)
   phpMyAdmin (Web GUI)
    `mysql` command-line client

Steps to Import the Schema:
1.  Clone the repository or download the `clinic_booking_system_schema.sql` file.
2.  Create a new database (Optional - if not already created):
    You can do this via your MySQL client. For example, using the command line:
    ```bash
    mysql -u your_username -p -e "CREATE DATABASE clinic_booking_system;"
    ```
    (Replace `your_username` with your MySQL username. You will be prompted for your password.)
    The SQL script itself contains commented-out lines to create the database if you uncomment them.
3.  Select the database:
    In your MySQL client, ensure you have selected the database you want to import the schema into.
    Command line:
    ```bash
    mysql -u your_username -p clinic_booking_system
    ```
    Then, once inside the mysql prompt:
    ```sql
    USE clinic_booking_system;
    ``
4.  Execute the SQL script:
    You can execute the `clinic_booking_system_schema.sql` file to create all tables and relationships.

    Using MySQL Workbench or DBeaver:
        1.  Connect to your MySQL server.
        2.  Open the `clinic_booking_system_schema.sql` file (File > Open SQL Script...).
        3.  Ensure the correct database/schema is selected as the default.
        4.  Execute the script (usually a lightning bolt icon or similar).

    Using the `mysql` command-line client:
        Navigate to the directory where you saved `clinic_booking_system_schema.sql` and run:
        ```bash
        mysql -u your_username -p clinic_booking_system < clinic_booking_system_schema.sql
        ```
        (This command imports the script directly into the `clinic_booking_system` database.)

 Entity Relationship Diagram (ERD)

You can generate a visual ERD from the provided SQL schema using various database tools.

Recommended Tools for ERD Generation:

MySQL Workbench: Use the "Reverse Engineer" feature (Database > Reverse Engineer) after importing the schema.
dbdiagram.io: A free online tool where you can paste the SQL DDL (CREATE TABLE statements) to generate an ERD.
Lucidchart: Offers database diagramming tools with SQL import capabilities.
