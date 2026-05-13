# PASTA Threat Model – Sneaker Marketplace App

## Project Description

In this exercise, I applied the PASTA threat modelling framework to assess the security risks of a mobile sneaker marketplace app. The app allows users to sign up, log in, search for sneakers, message sellers, rate sellers, and complete purchases.

The goal of this assessment was to identify business objectives, technical risks, potential threats, vulnerabilities, and security controls that could reduce the likelihood of a data breach or account compromise.

---

## Framework Used

**PASTA** stands for **Process for Attack Simulation and Threat Analysis**.

It is a threat modelling framework used to identify and analyse security risks in applications before they are exploited by attackers.

The seven stages are:

1. Define business and security objectives  
2. Define the technical scope  
3. Decompose the application  
4. Perform threat analysis  
5. Perform vulnerability analysis  
6. Model attacks  
7. Analyse risk and impact  

---

## Stage I: Business and Security Objectives

The sneaker marketplace app needs to allow users to:

- Sign up and log in securely
- Manage user accounts
- Search for sneakers
- Message sellers
- Rate sellers
- Complete purchases using multiple payment options

Data privacy is a key business concern because the app handles sensitive user and payment information. Secure payment handling is also important to reduce legal, financial, and reputational risk.

---

## Stage II: Technical Scope

The application uses several technologies, including:

- API
- Public Key Infrastructure (PKI)
- AES encryption
- RSA encryption
- SHA-256 hashing
- SQL database

I would prioritise SQL because the app relies on a database to store and retrieve user accounts, sneaker listings, seller information, and purchase data. If SQL queries are not handled securely, attackers could attempt SQL injection to access, alter, or delete sensitive information. This makes the database a high-risk part of the application.

---

## Stage III: Application Decomposition

The data flow diagram shows a user submitting a product search request to the application. The application then queries the database and returns current sneaker listings to the user.

This process involves:

- User input
- Backend processing
- Database access
- Returned product results

Because user input is passed into a process that interacts with the database, secure input validation and query handling are important.

---

## Stage IV: Threat Analysis

Potential threats include:

1. **SQL injection attack**  
   An attacker could attempt to inject malicious SQL through product search, login, or account input fields.

2. **Session hijacking or account takeover**  
   An attacker could attempt to steal session data or use weak credentials to gain access to user accounts.

These threats are significant because the app handles user data, payment activity, and marketplace transactions.

---

## Stage V: Vulnerability Analysis

Potential vulnerabilities include:

1. **Lack of prepared statements or poor input validation**  
   This could allow attackers to submit malicious input that is interpreted as SQL code.

2. **Weak authentication or insecure session handling**  
   Weak passwords, missing multi-factor authentication, or poor session controls could allow attackers to compromise user accounts.

---

## Stage VI: Attack Modelling

The attack tree shows that user data could be compromised through SQL injection or session hijacking.

SQL injection may occur if the application does not use prepared statements or fails to validate user input. Session hijacking may occur if login credentials are weak, session tokens are not protected, or session management is insecure.

Possible attack paths include:

- Attacker enters malicious SQL into a search or login field
- Application passes unsafe input to the database
- Database returns sensitive data or allows unauthorised changes
- Attacker uses stolen or weak credentials to access user accounts
- Attacker hijacks an active session and performs actions as the user

---

## Stage VII: Risk Analysis and Security Controls

Recommended controls include:

1. **Prepared statements**  
   Use prepared statements to separate SQL code from user input and reduce the risk of SQL injection.

2. **Multi-factor authentication (MFA)**  
   Require users to verify their identity using more than one factor, especially for account changes and payment-related actions.

3. **Strong password and session management controls**  
   Enforce strong password policies, secure session tokens, automatic session expiry, and protection against session hijacking.

4. **Encryption of sensitive data**  
   Use AES encryption for sensitive stored data and TLS for data in transit. Hash passwords securely using strong hashing practices.

---

## Key Skills Demonstrated

- Threat modelling using the PASTA framework
- Secure application risk analysis
- SQL injection risk identification
- Authentication and session security awareness
- Data flow analysis
- Security control recommendation
- Business risk communication

---

## Summary

This threat model identified key risks in a sneaker marketplace app that handles user data, seller communication, product listings, and payment activity. The highest-risk areas include database access, user authentication, and session security.

By applying controls such as prepared statements, multi-factor authentication, strong session management, and encryption, the organisation can reduce the likelihood of data breaches, account compromise, and unauthorised access.