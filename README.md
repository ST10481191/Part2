
# PROG5121 Part 2: QuickChat Application

 Overview
This project represents **Part 2** of the PROG5121 Portfolio of Evidence (POE). It expands upon the login and registration system from Part 1 to implement a fully functional Java console-based messaging system. The application enforces access control, validates messages and recipient phone numbers, generates unique message identifiers and uppercase hashes, provides interactive console menu options, and persists message data locally using JSON.

---

Features & Assignment Requirements Met
* **Access Control:** Requires successful authentication via the `Login` class before granting entry to the QuickChat menu loop.
* **Interactive Console Menu:** Implemented with a `do-while` loop presenting numeric choices:
  1. Send Messages
  2. Show recently sent messages ("Coming Soon.")
  3. Quit (exits and displays total sent count)
* **Message Entry & Validation:**
  * **Message ID:** Generates a unique 10-digit tracking number retaining leading zeroes.
  * **Recipient Validation:** Ensures phone numbers start with an international dialing code (e.g., `+27`) and meet valid length rules.
  * **Message Length:** Enforces the strict requirement that message text must be under 250 characters.
  * **Automated Hashing:** Dynamically generates an uppercase message hash using the first two ID digits, a zero-based message counter, and boundary words (e.g., `00:0:HITONIGHT`).
* **Message Processing Options:**
  * **Option 1 (Send):** Confirms successful delivery and increments the session's sent message total.
  * **Option 2 (Disregard):** Prompts for deletion confirmation.
  * **Option 3 (Store):** Persists message data into `messages.json` while maintaining existing records.
* **Unit Testing:** Comprehensive JUnit test suites (`LoginTest` and `MessageTest`) covering all success and failure conditions for inputs, hashes, and storage features.

---

Version Control & Commit History
To satisfy the POE version control and rubric requirements, the repository's commit history reflects structured, incremental development across **6 distinct commits**:

1. **Initial Commit:** Repository initialization, directory layout, and baseline structure.
2. **Part 1 Implementation:** Addition of user registration, username constraints, password complexity checks, and login verification.
3. **Core Message Setup:** Creation of the `Message` class architecture and 10-digit ID generation logic.
4. **Validation & Hashing:** Implementation of international phone number verification and uppercase message hashing rules.
5. **Console Menu & Processing:** Integration of the `do-while` interactive menu loop and option handlers (Send, Disregard, Store).
6. **JSON Storage & Testing:** Implementation of `messages.json` file writing/persistence and finalization of JUnit test suites.

---

Getting Started & Execution
1. Open **Apache NetBeans** (or your preferred Java IDE).
2. Open or import the project directory.
3. Right-click **`Main.java`** and select **Run File**.
4. Follow the console instructions to register, authenticate, and manage messages.

---

 References
* Deitel, H. and Deitel, P., 2017. *Java: How to Program (Early Objects)*. 11th ed. Harlow: Pearson.
* Horstmann, C.S., 2019. *Core Java Volume I–Fundamentals*. 11th ed. Boston: Pearson.
* The Independent Institute of Education (IIE), 2026. *PROG5121 Module Manual and POE Guidelines*. Johannesburg: IIE Rosebank College.

```
