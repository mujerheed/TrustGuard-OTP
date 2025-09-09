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

## 🚀 Workflow

### 🔹 Buyer Flow
1. Buyer sees product → sends a DM to vendor.
2. Business bot requests buyer details:  
   - Name  
   - Phone Number  
   - Address  
3. OTP is generated & sent via WhatsApp, SMS, or Email.  
4. Buyer enters OTP → verified as genuine.  
5. Buyer transfers payment & sends receipt/alert to vendor.  

---

### 🔹 Vendor Flow
1. Vendor receives buyer’s details and payment receipt.  
2. TrustGuard verifies if the receipt/alert is **real** (rule-based + AI fraud detection).  
3. Vendor confirms transaction or rejects if fake.  
4. Vendor manages orders via a **dashboard** (OTP login).  

---

### 🔹 CEO Flow (High-Value Transactions)
1. If transaction > defined threshold (e.g., $1000), CEO intervention is required.  
2. CEO logs into the dashboard with a **digit-based OTP** (higher privilege).  
3. CEO approves or rejects large transactions.  
4. CEO manages vendor accounts, buyer logs, and transaction records.  

---

## 📂 Project Structure
```plaintext
TrustGuard/
│── README.md               # Project description
│── requirements.txt        # Python dependencies
│── .env.example            # Environment variables template
│── app/
│   ├── __init__.py
│   ├── main.py             # Flask/FastAPI entry point
│   ├── config.py           # Configurations (DB, API keys, etc.)
│   ├── models.py           # Database models
│   ├── routes/
│   │   ├── buyer.py        # Buyer OTP & order routes
│   │   ├── vendor.py       # Vendor verification routes
│   │   ├── ceo.py          # CEO approval routes
│   ├── services/
│   │   ├── otp_service.py  # OTP generation & verification
│   │   ├── fraud_service.py# Fake receipt detection
│   │   ├── email_service.py# Email/SMS/WhatsApp integration
│   ├── templates/          # HTML templates (if Flask Jinja2 used)
│   └── static/             # CSS/JS assets (later for dashboard)
│
│── database/
│   ├── schema.sql          # Initial DB schema
│   └── migrations/         # Future DB migrations
│
│── tests/
│   ├── test_buyer.py
│   ├── test_vendor.py
│   └── test_ceo.py
│
│── docs/
│   ├── architecture.md     # System design docs
│   ├── workflow.md         # Business process workflow
│   └── api_endpoints.md    # API documentation
```

## Installation Guide

## Demo Screenshots