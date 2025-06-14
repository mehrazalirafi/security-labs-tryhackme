
# SQL Injection Attack Summary

## What is Code Injection?

- **Definition**: Code injection involves adding your own data into a data stream.
- **Cause**: Primarily due to bad programming—applications should validate input and output properly.
- **Injection Vectors**: HTML, SQL, XML, LDAP, etc.

![Code Injection](./54e3a9d0-281c-42e5-99b7-c827812f3ad9.png)

---

## SQL Injection (SQLi)

- **SQL**: Structured Query Language — the most common language used for relational database queries.
- **SQLi Explained**: 
  - Attackers inject their own SQL statements into an application's input field.
  - These queries are then executed by the database.
  - The application should validate input and block such behavior.
- **Common Attack Vector**: Web browser form or field.

![SQL Injection Intro](./afbe3697-7adb-4de2-a7e1-9b4a0e9ae8c4.png)

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

![SQL Injection Code](./17ca5976-e041-47c3-a7f1-29317cc35946.png)

---

## SQL Injection Demonstration: Normal Query

- Employee `Smith` with TAN `3SL99A` is queried.
- Only Smith's data is returned.

![SQL Injection Normal Result](./b9992f1b-50dc-4892-92e4-7ba4a34a5960.png)

---

## SQL Injection Demonstration: Injected Code

- Input changed to include:
  ```sql
  ' OR '1' = '1
  ```
- **Result**: Full database output including other employees and sensitive information.

![SQL Injection Exploit Result](./3d962665-fa42-4af5-b92a-a5bdf5bc4ca3.png)

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

> Source: Professor Messer – [professormesser.com](https://professormesser.com)
