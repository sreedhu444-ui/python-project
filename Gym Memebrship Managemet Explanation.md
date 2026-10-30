# Gym Membership Management System

**Major project:** Gym Management System using Python 3 and SQLite  

## Project overview

This application manages gym members, membership plans, assigned memberships,
payment status, and login accounts. It demonstrates database design, primary
and foreign keys, SQL CRUD operations, authentication, role-based permissions,
input validation, and exception handling.

## Requirements

* Python 3.x
* SQLite3 (included with Python)



## Files to submit

* `gym\_management.py` — complete Python source code
* `gym\_management.db` — SQLite database with sample records
* `README.md` — setup and usage instructions

## How to run

1. Save all three files in the same folder.
2. Open a terminal or Command Prompt in that folder.
3. Run `python gym\_management.py` (or `python3 gym\_management.py`).
4. The program creates the database and tables automatically if needed.

## Demo login accounts

|Role|Username|Password|
|-|-|-|
|Administrator|`admin`|`Admin@123`|
|Staff|`staff`|`Staff@123`|

The database stores salted PBKDF2 password hashes, not plain-text passwords.
Public registration creates Staff accounts only. Use the demo credentials for
project testing; change them before any real deployment.

## Features

* Registration, login, and logout
* Admin and Staff role-specific menus
* Admin can add, view, update, and delete members and membership plans
* Staff can view/add members, view plans, assign memberships, view memberships,
and update payment status
* Assign a plan to a member and calculate the membership end date
* Track Paid/Pending payment status
* Validation for blank fields, numeric values, dates, menu options, and IDs
* Duplicate checks for usernames, member phone numbers/emails, and plan names
* Exception handling for SQLite errors and invalid input
* Parameterized SQL statements and foreign-key enforcement

## Database design

Four tables are used:

1. `users` — user name, password salt/hash, and role
2. `members` — member contact details, join date, status, and creator
3. `plans` — plan name, duration, price, and description
4. `memberships` — member/plan links, start/end dates, and payment status

## Sample records

First-time setup creates Monthly, Quarterly, and Annual plans, one sample member
and membership, and demo Admin/Staff accounts. These are sample data for testing.

## Suggested test plan

1. Log in as Admin and view the sample member and plans.
2. Add a member, then try a duplicate phone number.
3. Update and delete a test member.
4. Assign a membership and verify the end date.
5. Change a payment from Paid to Pending.
6. Log out and log in as Staff; verify that plan/member deletion options are
unavailable in the Staff menu.
7. Try incorrect login details and invalid menu choices.
8. Exit and restart the application; confirm data persists.

## Concepts demonstrated

Variables, data types, functions, loops, conditional statements, lists/dictionaries,
the `sqlite3` module, `CREATE TABLE`, `INSERT`, `SELECT`, `UPDATE`, `DELETE`,
joins, primary keys, foreign keys, authentication, role-based authorization,
input validation, and exception handling.

