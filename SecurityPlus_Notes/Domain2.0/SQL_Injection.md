
# SQL Injection Attack Summary

## What is Code Injection?

- **Definition**: Code injection involves adding your own data into a data stream.
- **Cause**: Primarily due to bad programming—applications should validate input and output properly.
- **Injection Vectors**: HTML, SQL, XML, LDAP, etc.

---

## SQL Injection (SQLi)

- **SQL**: Structured Query Language — the most common language used for relational database queries.
- **SQLi Explained**: 
  - Attackers inject their own SQL statements into an application's input field.
  - These queries are then executed by the database.
  - The application should validate input and block such behavior.
- **Common Attack Vector**: Web browser form or field.

---

## Example of SQL Injection

- Website code might resemble:
  ```sql
  SELECT * FROM users WHERE name = '" + userName + "';
  ```
- If a user enters **Professor**, the query becomes:
  ```sql
  SELECT * FROM users WHERE name = 'Professor';
  ```
- If an attacker inputs:
  ```sql
  ' OR '1' = '1
  ```
  The query becomes:
  ```sql
  SELECT * FROM users WHERE name = 'Professor' OR '1' = '1';
  ```
- **Result**: Bypasses authentication and exposes the entire database.

---

## SQL Injection Demonstration: Normal Query

- Employee `Smith` with TAN `3SL99A` is queried.
- Only Smith's data is returned.

---

## SQL Injection Demonstration: Injected Code

- Input changed to include:
  ```sql
  ' OR '1' = '1
  ```
- **Result**: Full database output including other employees and sensitive information.

---

## Why It’s Dangerous

- SQL injections allow attackers to:
  - View or delete all database data
  - Modify or corrupt records
  - Perform Denial of Service (DoS)
  - Add unauthorized users or backdoors

## Prevention Tips

- Use **prepared statements** or **parameterized queries**
- Validate and sanitize all user inputs
- Employ **least privilege** for database access
- Use a **Web Application Firewall (WAF)**

---
