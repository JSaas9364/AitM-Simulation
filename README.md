# AitM-Simulation

Adversary-in-the-Middle (AitM) attack simulation in a Windows AD environment.  
This project demonstrates traffic redirection using a phishing payload and Burp Suite proxy interception.

---

## 📁 Project Structure

AitM-Simulation/<br/>
├── README.md<br/>
├── Configure Burpsuite with 203.docx<br/>
├── Configure Burpsuite with 203.pdf<br/>

---

## 🛠️ Tools Used

- **Burp Suite** (proxy interception & traffic inspection)
- **Custom BAT script** (sets proxy to `203.0.113.66:8080`)
- **Windows 10 target machine**
- **Phishing delivery method** (malicious email payload)

---

## 🧪 Attack Overview

1. **Proxy Setup**:  
   - Burp Suite is configured to listen on `203.0.113.66:8080`
   - Intercept mode is turned off for passive traffic logging

2. **Payload Delivery**:  
   - A phishing email is sent to the victim
   - Victim executes a `.bat` file that reconfigures system proxy settings to route traffic through Burp

3. **Capture Phase**:  
   - All outbound HTTP/S traffic from the victim flows through the attacker’s proxy
   - Sensitive data is logged in Burp’s **HTTP history**, particularly under MIME type: `Post`

---

## 📄 Full Attack Walkthrough (PDF)

➡️ [View PDF Report](./Configure%20Burpsuite%20with%20203.pdf)

The PDF includes step-by-step setup instructions, screenshots of proxy behavior, and traffic analysis results from Burp Suite.

---

## ⚠️ Disclaimer

This project is for educational use in controlled lab environments only.  
Do **not** simulate AitM attacks on production systems or networks you do not own.

---
