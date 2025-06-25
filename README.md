# Jeyhlin-Jaftha-ST10472428-POE
# 📱 QuickChat Messaging System – PROG5121 PoE

This project is a messaging system developed as part of the Programming 1A (PROG5121) Portfolio of Evidence. It includes user registration and login, message creation and validation, array storage, JSON file handling, and full unit test automation via GitHub Actions.

---

##  Features

###  User Login System
- Register with username, password, and phone number
- Validation checks:
  - Username: must include `_` and be ≤ 5 characters
  - Password: must include uppercase, number, special character, and be ≥ 8 characters
  - Phone number: must start with `+27` and be ≥ 12 digits

###  Message System
- Create messages with a recipient number and message body
- Each message is assigned:
  - A 10-digit random message ID
  - A custom hash using the first and last words of the message

- User options:
  - **Send**: saves to a sent message array
  - **Store**: saves to `storedMessages.json` using Gson (as a JSON array)
  - **Disregard**: discards the message

###  Message Management (Part 3)
- Display all senders/recipients
- Find the longest message
- Search messages by ID or recipient
- Delete messages by hash
- Print a full message report

---

##  Unit Testing

### `MessageTest.java`
Covers:
- Message length and recipient validation
- Message ID and hash generation
- Send counter
- Searching and deleting
- Loading from JSON

### `LoginTest.java` (optional)
Tests username, password, and phone validation logic.

---

##  CI/CD with GitHub Actions

### `.github/workflows/TestJava.yml`
- Automatically runs unit tests on push/pull to `main`
- Uses Java 17 and Maven

---

## Files Included

| File                  | Description                            |
|-----------------------|----------------------------------------|
| `MainApp.java`        | Main entry point (login + launch)      |
| `Login.java`          | Handles validation logic               |
| `LoginTest.java`      | Tests for login functionality          |
| `Message.java`        | Core message creation and logic        |
| `MessageSystem.java`  | Manages user input and message flow    |
| `MessageTest.java`    | Unit tests for message functionality   |
| `storedMessages.json` | Stored messages in JSON format         |
| `.github/workflows/`  | GitHub Actions CI setup                |

---

##  How to Run

1. Open project in NetBeans or IntelliJ
2. Run `MainApp.java` to start
3. Run unit tests via test folder or GitHub Actions

---

##  Notes

- All JSON is handled using Google's Gson library
- All validation and reporting follows PoE rubric requirements
- Attribution: JSON loading logic adapted using ChatGPT support

---
