# TrustGuard: A Zero-Trust OTP Verification System for Informal Social Media E-commerce  

## 🔹 Project Overview  
In Nigeria, Social media vendors uses **WhatsApp, Instagram, Facebook** as informal e-commerce platforms using posts, reels, or statuses.  
Customers places order via **DMs**, payment done by **bank transfer**, and send **receipts or alert message screenshot** as proof.

**🔹 Problem:**  
- Difficult to verify if a customer or vendor is genuine.  
- Payment receipts can be fake (edited screenshots).
- No authentication or verification layer before transactions.   

**🔹 Proposed Solution:**  
This project introduces **TrustGuard**, a security system based on:  
- **OTP Authentication (alphanumeric code via email/SMS)**  
- **Least Privilege Access (Zero Trust security model)**  
- **Optional receipt validation (hashing / transaction lookup)**  

The goal is to **increase trust** in social media e-commerce transactions, while serving as a **project-based learning system** for cybersecurity students.  

---

## 🔹 Features  
✅ OTP-based customer verification  
✅ Vendor dashboard with Zero Trust principles  
✅ Role-based least privilege (customer/vendor/admin)  
✅ High-value transactions require CEO OTP approval  
✅ Secure receipt validation (optional module)  
✅ Cloud-ready deployment (AWS/GCP/Azure)  

---

## 🔹 System Architecture  

```plaintext
Customer (WhatsApp/Instagram/FB)  
    ↓  
TrustGuard App (Web/Mobile Interface)  
    ↓  
OTP Service (Email/SMS)  
    ↓  
Vendor Dashboard (Zero Trust Access Control)  
    ↓  
Admin/CEO (High-Value Approval via OTP)  
```

## 🔹Tech Stack

- Backend: Python (Flask / FastAPI / Django)
- Frontend: React.js / Flask templates
- Database: PostgreSQL / MySQL
- Security: JWT, RBAC, PyOTP, Hashlib
- Cloud Deployment: AWS / GCP / Azure
- Optional Services: Twilio (SMS OTP), SendGrid (Email OTP)