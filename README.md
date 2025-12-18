Invoice Management System v2 (Flask + MySQL)
A fully working Invoice Management System built with:

Frontend: HTML, CSS, Vanilla JavaScript

Backend: Python Flask REST API

Database: MySQL

Currency: Indian Rupees (₹)

The system supports client management, invoice creation with GST, dashboard analytics, and print-friendly invoice views.

Features
Client Management
View existing clients

Add new clients with validation:

Minimum 2 characters

Trimmed input

Case-insensitive duplicate check

Preloaded sample clients:

TCS

Infosys

Wipro

HCL

Accenture

Invoice Management
Create invoices with:

Client dropdown populated from database

Customer email and billing address

Invoice date and due date

Multiple line items (add/remove rows)

Per-line GST percentage

Automatic calculation of:

Subtotal

GST total

Grand total (₹)

View invoices:

Detailed invoice view with:

Invoice number

Client details

Billing address

Line items

GST breakdown

Subtotal, GST, Grand Total

Delete invoices:

Confirmation dialog before deletion

Cascade delete of line items

Print invoices:

Print button triggers window.print()

Print-optimized CSS hides navigation and buttons

Clean invoice layout for printing or generating PDF

Dashboard
Total number of invoices

Total revenue (₹)

Pending amount (₹) based on status Pending

Recent invoices table with:

Invoice number

Client name

Amount

Date

Status badge (Draft / Pending / Paid)

View and Delete actions

Navigation & UX
Left sidebar navigation:

Dashboard

Create Invoice

All Invoices

Manage Clients

Right panel shows corresponding content with JavaScript show/hide logic

No page reloads while navigating between sections

Project Structure
text
invoice-management-v2/
├── app.py
├── schema.sql
└── templates/
    └── index.html
app.py – Flask application with REST APIs

schema.sql – MySQL database schema and sample data

templates/index.html – Single-page frontend UI

Requirements
Python 3.8+

MySQL Server

pip (Python package manager)

Python packages:

Flask

mysql-connector-python

flask-cors (optional but included for flexibility)

Setup Instructions
1. Clone the Repository
bash
git clone <your-repo-url>.git
cd invoice-management-v2
2. Create MySQL Database
Log in to MySQL and run the schema file:

bash
mysql -u root -p < schema.sql
This will:

Create database invoice_db_v2

Create tables: clients, invoices, invoice_items

Insert sample clients (TCS, Infosys, Wipro, HCL, Accenture)

If your MySQL user/password or host is different, adjust accordingly.
