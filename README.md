# SENTRY — Authentication Security Toolkit

SENTRY is an interactive browser-based authentication security toolkit designed to demonstrate common authentication defenses and attack-detection techniques.

The project provides **five interactive security modules** covering password security, account protection, secure password generation, brute-force detection, and password-guessing detection.

---

## Features

### 1. Password Strength Checker

Evaluates passwords against five security criteria:

* Minimum 8 characters
* At least one uppercase letter
* At least one lowercase letter
* At least one number
* At least one special character

The password receives a score from **0–5** and is classified as Very Weak, Weak, Moderate, Strong, or Very Strong.

### 2. Login Lockout Simulator

Demonstrates protection against repeated failed login attempts.

* Maximum of 3 login attempts
* Tracks remaining attempts
* Locks the account after the third failed attempt
* Displays a session log
* Provides a session reset option

The demo login credentials are configured directly in the client-side simulation.

### 3. Secure Password Generator

Generates random passwords based on user-selected requirements.

Supported character classes:

* Uppercase letters
* Lowercase letters
* Numbers
* Special characters

The generator guarantees at least one character from every selected class and uses `crypto.getRandomValues()` for random number generation before shuffling the generated characters.

### 4. Brute-Force Attack Detection

Analyzes login records in the format:

```text
ip,status
```

The system counts failed attempts for each IP address and flags an IP when it reaches **3 or more failed attempts**.

The module generates:

* Records processed
* Total failed attempts
* Flagged IP addresses
* Security alerts
* Detection table

### 5. Password Guessing Detection

Analyzes login records in the format:

```text
username,password,status
```

The system tracks distinct failed passwords for each username and identifies accounts targeted with **3 or more different passwords**.

## This helps distinguish targeted password-guessing behavior from repeated attempts using the same incorrect password.

## Technologies Used

* HTML5
* CSS3
* JavaScript
* Web Crypto API
* Responsive Web Design
* Cybersecurity concepts
* Authentication security concepts

---

## Project Structure

```text
SENTRY/
│
├── index.html
└── README.md
```

The current implementation is contained in a single HTML file with embedded CSS and JavaScript.

---

## How to Run

### Option 1 — Browser

1. Download or clone the repository.
2. Open `index.html`.
3. The SENTRY toolkit will load directly in your browser.
4. Select any module from the navigation panel.
5. Test the security functions using the provided inputs and sample data.

### Option 2 — VS Code

1. Open the project folder in VS Code.
2. Open `index.html`.
3. Use **Live Server** or open the file directly in a browser.
4. Interact with the five security modules.

---

## Sample Detection Logic

### Brute-Force Detection

```text
IP Address        Failed Attempts
192.168.1.10      4
198.51.100.23     3
```

Both addresses are flagged because they exceed the configured three-failure threshold.

### Password Guessing Detection

```text
Username     Distinct Passwords
jsmith       3
tomlin       4
```

These accounts are flagged because multiple different passwords were attempted against the same username.

---

## Security Concepts Demonstrated

* Password policy enforcement
* Authentication controls
* Account lockout
* Password generation
* Brute-force attack detection
* Password-guessing detection
* Threshold-based threat detection
* Security event logging
* Input validation
* Client-side security simulation

---

## Disclaimer

SENTRY is an **educational security simulation** created to demonstrate authentication security concepts. It is not intended to replace production authentication, password-management, intrusion-detection, or account-security systems.

---

## Author

**Sahasra Kotte**

B.Tech — Information Technology
VNR Vignana Jyothi Institute of Engineering and Technology
