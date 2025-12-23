# 🔐 Secure VPN System using ECDH and AES-GCM

A **Python-based Secure VPN System** that enables **encrypted communication** between a client and a server using modern cryptographic techniques.
The system uses **Elliptic Curve Diffie-Hellman (ECDH)** for secure key exchange and **AES-256-GCM** for authenticated data encryption.

This project supports:

* 🔑 Secure key exchange without key transmission
* 🔒 End-to-end encrypted communication
* 🌐 Secure web request tunneling
* 🛡️ Protection against eavesdropping & tampering
* 🧪 Demonstration of real-world VPN fundamentals

---

## 📌 Project Overview

Public networks are vulnerable to **packet sniffing, tampering, and man-in-the-middle attacks**.
This project demonstrates how a VPN establishes a **secure tunnel** over an insecure network.

The system:

1. Performs secure key exchange using ECDH
2. Derives a shared symmetric encryption key
3. Encrypts all communication using AES-GCM
4. Forwards web requests securely through the server
5. Returns encrypted responses to the client

---

## 🎯 Key Objectives

* Demonstrate secure VPN fundamentals
* Implement encrypted client-server communication
* Prevent man-in-the-middle attacks
* Ensure data confidentiality and integrity
* Understand real-world cryptographic workflows

---

## 🧠 Cryptographic Concepts Used

| Concept            | Purpose                       |
| ------------------ | ----------------------------- |
| ECDH               | Secure key exchange           |
| AES-256-GCM        | Fast authenticated encryption |
| PBKDF2             | Secure key derivation         |
| Nonce              | Prevent replay attacks        |
| Authentication Tag | Detect tampering              |

---

## 🏗️ System Architecture

```
VPN Client
    ↓ (Public Key Exchange)
ECDH Key Agreement
    ↓
Shared Secret
    ↓
PBKDF2 Key Derivation
    ↓
AES-256-GCM Encrypted Tunnel
    ↓
VPN Server → Internet
```

---

## 🔄 VPN Communication Workflow

1. Client connects to VPN server
2. Client & server exchange public keys
3. Shared secret generated using ECDH
4. AES-256 key derived using PBKDF2
5. User verifies shared key (extra security layer)
6. Client sends encrypted web request
7. Server decrypts, fetches data
8. Server encrypts response and sends back
9. Client decrypts and opens result

---

## 🔐 Security Features

✔ No encryption key sent over network
✔ Authenticated encryption (confidentiality + integrity)
✔ Random nonce for every message
✔ Manual shared-key verification (extra authentication)
✔ Resistant to MITM & replay attacks

---

## ⚙️ Technology Stack

### Backend & Networking

* 🐍 Python
* 🔌 Socket Programming
* 🌐 Requests Library

### Cryptography

* 🔐 cryptography (Python)
* 🔑 ECDH (SECP256R1)
* 🔒 AES-256-GCM
* 🔁 PBKDF2-HMAC-SHA256

### Client Interface

* 🖥️ Tkinter (secure key entry)
* 🌍 Webbrowser module

---

## 🛠️ Installation & Setup

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/secure-vpn-system.git
cd secure-vpn-system
```

### 2️⃣ Install Dependencies

```bash
pip install cryptography requests
```

### 3️⃣ Start VPN Server

```bash
python vpns1.py
```

### 4️⃣ Start VPN Client

```bash
python vpnc1.py
```

---

## 📂 Project Structure

```
├── vpns1.py
├── vpnc1.py
├── requirements.txt
└── README.md
```

---

## ⚠️ Limitations

* Single client at a time
* Not a full packet-level VPN
* Limited to HTTP URL forwarding
* No user authentication database

---

## 🚀 Future Enhancements

* Multi-client support
* Full HTTP/HTTPS tunneling
* Authentication with username/password
* Traffic compression
* Logging & monitoring dashboard
* Deployment using Docker

---

## 🎓 Academic Relevance

This project is suitable for:

* Cryptography & Network Security coursework
* VPN & Secure Communication demonstrations
* Final Year Mini Project
* Resume & Interview Portfolio

---

## 👨‍💻 Author

**Benny Christiyan**
B.Tech Computer Science & Engineering