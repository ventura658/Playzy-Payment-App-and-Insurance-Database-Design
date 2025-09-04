# Assignment 2: Insurance Database Redesign Solution

## Overview
This document outlines the database design for the insurance system. It includes the key tables, their attributes, data types, primary keys, foreign keys, and relationships based on the provided solution.

## Table Diagram
To visualize the database schema, refer to the image below. This could be an ERD (Entity-Relationship Diagram) or a table structure diagram.

![Insurance Database Table](https://github.com/ventura658/Playzy-Payment-App-and-Insurance-Database-Design/blob/5d7e6924a9b529445a777672a774402945cfeac3/Insurance-Database-Design/Ex1-2.png)


## Database Tables

- **Insured Table**: Stores information about insured individuals, including the AMKA (Social Security Number), name, date of birth, gender, and contact details. The primary key is the AMKA.

- **Parent_of_Insured Table**: Connects insured individuals with their parents, specifying the relationship (e.g., Mother or Father). This table likely includes foreign keys to the Insured table for both the child and parent AMKA.

- **Disease Table**: Contains information about diseases, including a unique disease code, name, and symptoms.

- **Doctor Table**: Stores information about doctors, including their AMKA, name, specialty, professional address, and contact details. The AMKA is a foreign key from the Insured table. A composite key is defined using the name, last name, and specialty.

- **Doctor_Visits Table**: Records visits between doctors and insured patients, including the date of the visit. The primary key is a composite key consisting of the patient's AMKA and the visit date. The AMKA is a foreign key from the Insured table.

## Relationships
- One doctor can coordinate multiple (N) visits, so the doctor's composite key (e.g., name, last name, and specialty) is included in the Doctor_Visits table.
- One disease can be associated with multiple (N) visits, so the primary key of the Disease table is included in the Doctor_Visits table.
- One insured person can have multiple (N) visits, so the primary key of the Insured table (AMKA) is included in the Doctor_Visits table.

This schema ensures proper tracking of insured individuals, their relationships, diseases, and medical visits
