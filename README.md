# Penetration Testing: Password Cracking & Hash Extraction (Week 3)

## 📌 Project Overview
This repository contains the documentation for the Week 3 practical labs of the Networkwalks Cybersecurity Program. The objective was to demonstrate the vulnerabilities of weak passwords by extracting cryptographic hashes from locked PDF documents and recovering the plaintext passwords using dictionary attacks.

## 🚀 Modules Completed
*   **W3-PM1 (Password Cracking with JTR):** Utilizing the industry-standard John the Ripper (JTR) via the Johnny graphical interface installed natively on Kali Linux.
*   **W3-PM2 (Password Cracking with NW Tools):** Utilizing the Networkwalks Hash Calculator and web-based dictionary attack environment.

## 🛠️ Tools & Technologies Used
*   **Environment:** Physical Kali Linux host machine.
*   **Local Tools:** Linux Terminal, John the Ripper, Johnny GUI.
*   **Web Tools:** OnlineHashCrack.com, Networkwalks Hash Calculator & Password Cracker.
*   **Target:** Password-protected file `My-Locked-PDF1.pdf`.

## 📝 Execution Steps & Methodology

### Approach 1: Local Cracking with John the Ripper & Johnny GUI (W3-PM1)
1.  **Hash Extraction:** The locked PDF was submitted to an extraction tool, generating a fingerprint compatible with the `$pdf$` format.
2.  **File Preparation:** Created the `hash1.txt` file containing the extracted hash via the terminal.
3.  **Cracking:** The Johnny interface was configured to target the native John the Ripper executable. The dictionary attack tested a list of common words and successfully revealed the plaintext password: `password1`.

### Approach 2: Web-Based Cracking (W3-PM2)
1.  **Hash Parsing:** Imported the locked PDF into the Networkwalks Hash Calculator.
2.  **Dictionary Attack:** Submitted the hash to the Password Cracker tool. The dictionary match confirmed the password `password1`.

### 🏁 Flag Capture
Using the recovered weak password, the PDF document's access protection was successfully bypassed.

![Entering the password](unlock.png)[cite: 35]

Opening the document revealed the congratulatory message and the hidden flag validating the exercise.

![Captured flag](Done.png)[cite: 34]

**Captured Flag:** `nw{networkwalks_flag1_jtr_270521_1}`[cite: 34]

## 📊 Conclusion
This exercise practically demonstrates the critical vulnerability of dictionary-based passwords. As a Master's student in Cryptography and Information Security, this lab serves as a concrete illustration that even the most robust mathematical encryption standards are instantly rendered useless if the underlying password (the human factor) lacks entropy and complexity.

## ⚠️ Legal Disclaimer
All activities documented in this project were performed strictly for educational purposes within an authorized and simulated lab environment.
