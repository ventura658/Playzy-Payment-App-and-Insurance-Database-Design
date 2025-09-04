# Playzy Payment App and Insurance Database Redesign

## Introduction
This repository contains descriptions for two assignments:
- **Assignment 1**: A payment application without cards, known as Playzy.
- **Assignment 2**: Redesign of the database for insured individuals.

Details of the assignments are provided below.

## Assignment 1: Playzy Payment Application
Playzy is an application for payments without the use of credit cards and electronic payments. It serves users who can pay for any transaction with any bank.

Playzy has access to the registry of merchants and banks that collaborate with the application. Each customer registers in the application by providing the following details: First name, last name, father's name, email address, mobile phone number, date of birth, and tax identification number (AFM). If the above details are not complete, the system displays an error message prompting the customer to contact the customer support department of the application.

Playzy offers each customer a digital wallet (DW) which has a unique address, equivalent to the IBAN of a bank account. The digital wallet stores the customer's money. Playzy allows the customer to view the contents of their DW at any time. Specifically, they can see the total amount in euros it contains and if they have any redemption points after using the application. Redemption points correspond to a total number and can be redeemed in euros.

The customer gains access to Playzy through their login credentials, with which they are authenticated by the system.

## Assignment 2: Insurance Database Redesign
There is a need to redesign the Database of the insured in the country. For each insured person, the following are stored: The insured's AMKA (Social Security Number), first name, last name, date of birth, gender, address (street, number, city, postal code), and phone number. Each insured person has at most one mother and one father, who must be registered in the insured persons' file.

Insured persons suffer from diseases. For each disease that exists, the following details must be recorded: Disease code, name, and symptoms.

Insured persons are divided into 2 categories:
- Directly insured individuals who have an insurance provider and indirectly insured individuals.
- Indirectly insured individuals are covered by one of their parents. It is noted that protected members have their own AMKA.

An insured person may also be a doctor. In this case, the following must additionally be recorded: Their specialty, the address of their medical office (street, number, city, postal code), and the phone number of the office. When an insured person falls ill, they visit the doctor who diagnoses a disease. For each visit, the date must be recorded.
