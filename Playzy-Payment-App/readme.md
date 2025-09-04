
# Assignment 1: Playzy Database Schema Solution

## Overview
This document outlines the database design for the Playzy payment application. It includes the key tables, their attributes, data types, primary keys, foreign keys, and relationships as described in the solution.

## Table Diagram
To visualize the database schema, refer to the image below. This could be an ERD (Entity-Relationship Diagram) or a table structure diagram.

![Playzy Database Table](https://github.com/ventura658/Playzy-Payment-App-and-Insurance-Database-design/blob/339f269c0a4b230628f5c4d4312912948b190290/Playzy-Payment-App/Ex1-1.png)

## Database Tables

- **Customers Table**: Stores information about customers, including the AFM (Tax Identification Number), full name, date of birth, phone number, and email. The primary key is the AFM.

- **Merchants Table**: Provides basic information about merchants, such as the name and a unique key (e.g., a merchant ID).

- **Banks Table**: Provides basic information about banks, such as the name and a unique key (e.g., a bank ID).

- **Transactions Table**: Stores information about transactions, including a unique ID key, the transaction date, the amount, and the three involved parties (customer, bank, and merchant). Foreign keys include the wallet address, the bank key, and the merchant key. The amount is defined as a DECIMAL with 10 significant digits and a default value of 0.00.

- **DigitalWallets Table**: Contains information about each customer's digital wallet, such as the current balance, reward points, and wallet address. The foreign key is the customer's AFM. The balance is a DECIMAL with 10 significant digits and a default value of 0.00, while the points are an INT with a default value of 0.

- **UserCredentials Table**: Consists of a unique username and the password used by the user to log in to the application. The foreign key is the customer's AFM.

## Relationships
- A transaction is associated with exactly 1 digital wallet, 1 merchant, and 1 bank.
- Each customer has exactly 1 username.
- Each customer has exactly 1 digital wallet.

This schema ensures data integrity and supports the core functionality of the Playzy application.
