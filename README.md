# 📱 Stockify — Smart Mobile Shop POS & ERP System

[![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20Web-green.svg)](https://capacitorjs.com/)
[![React](https://img.shields.io/badge/React-19.x-blue.svg?logo=react)](https://react.dev/)
[![Capacitor](https://img.shields.io/badge/Capacitor-7.x-119EFF.svg?logo=capacitor)](https://capacitorjs.com/)
[![Backend](https://img.shields.io/badge/Backend-Supabase%20PostgreSQL-3ECF8E.svg?logo=supabase)](https://supabase.io/)
[![Design](https://img.shields.io/badge/Design-Glassmorphism%20%26%20Framer%20Motion-FF69B4.svg)](https://framer.com/motion)
[![License](https://img.shields.io/badge/License-Proprietary%20%2F%20Closed--Source-red.svg)](#-proprietary-software-notice)

> 🔒 **Proprietary Software Notice:**  
> **Stockify** is a commercial software solution developed for retail mobile shops and electronics businesses. The core source code is maintained in a private repository. This repository serves as the **official public showcase, technical documentation, and release portal for APK testing**.

---

## 📲 Download & Test Android APK

You can test the full capabilities of **Stockify** directly on your Android phone:

👉 **[Download Latest Stockify Android APK Here](https://txhcdtownkvydrdxlmjd.supabase.co/storage/v1/object/public/App_release/Stockify%20version%203.4.4.apk)**  
*(Alternatively, insert your Google Drive / Direct APK download link here)*

> **Installation Tip:** When installing on Android for testing, allow "Install from Unknown Sources" if prompted by your browser/file manager.

---

## 🎥 Video Walkthrough & Screenshots

### 📹 Video Demo
<!-- Drop your YouTube, Loom, or direct MP4 demo video link below -->
> 🎬 **Demo Video:** *Coming Soon / Upload your demo video or link here*

---

### 📸 App Screenshots
<!-- You can drop your screenshots into a folder named /screenshots and link them below -->

| 🛒 Point of Sale & Billing | 📦 Inventory & Stock | 📒 Digital Khata (Ledger) |
|:---:|:---:|:---:|
| *(Add POS Screenshot)* | *(Add Inventory Screenshot)* | *(Add Khata Screenshot)* |

| 🔧 Mobile Repairing Desk | 📱 Used Phone Registration | 📊 Sales History & Analytics |
|:---:|:---:|:---:|
| *(Add Repairing Screenshot)* | *(Add Phone Register Screenshot)* | *(Add Analytics Screenshot)* |

---

## 💡 About Stockify

Managing a mobile retail business involves tracking high-value devices by **IMEI numbers**, dealing with hundreds of small accessories, handling **customer credit (Khata / Udhaar)**, tracking **repair jobs**, and complying with regulations when buying used phones.

**Stockify** is an all-in-one digital operating system engineered specifically to replace paper records, scattered registers, and complex desktop software with an intuitive, mobile-first experience.

---

## 🚀 Key Modules & Capabilities

### 1. 🛒 Point of Sale (POS) & Billing
- **Instant Product Lookup:** Search by device name, barcode, or scan IMEI directly using the device camera.
- **Integrated Hardware Scanning:** Powered by Capacitor Native Camera & ZXing barcode engine with realistic audio feedback.
- **Flexible Payment Methods:** Cash, EasyPaisa, JazzCash, Bank Transfer, or Khata (Credit).
- **Thermal & PDF Invoicing:** Automatic receipt formatting with instant one-click sharing via WhatsApp.

### 2. 📦 IMEI-Grade Inventory Control
- **Dual Category Engine:** Dedicated tracking for IMEI-bound smartphones vs. quantity-bound accessories.
- **Live Stock Alerts:** Real-time low-stock and out-of-stock indicators.
- **Stock Inward History:** Comprehensive history of purchase batches, supplier details, and cost prices.

### 3. 📒 Digital Khata & Customer Ledger
- **Customer Accounts:** Complete debit/credit ledger tracking for regular clients and dealers.
- **Transaction Logs:** Time-stamped history of loans, repayments, and balance summaries.
- **WhatsApp Statements:** Generate professional payment reminder slips.

### 4. 🔧 Mobile Repair Service Desk
- **Job Ticketing:** Issue repair job cards with customer details, device issues, passcode/pattern notes, and delivery commitments.
- **Status Lifecycle:** Step-by-step progress tracking (*Received ➔ Inspecting ➔ Fixed ➔ Delivered*).
- **Claim Receipts:** Professional claim slips with terms & conditions to prevent customer disputes.

### 5. 📱 Used Phone Purchase & Seller Verification
- **Identity Verification:** Record seller CNIC, phone number, and physical photo.
- **Digital Purchase Slips:** Protects shopkeepers against stolen phones with legally compliant digital seller agreements.

### 6. 📅 Installment (EMI) Management
- **Custom Installment Plans:** Define down payment, monthly installments, markup, and tenure.
- **Schedule Tracker:** Track upcoming, paid, and overdue installments at a glance.

### 7. 🔒 Biometrics & Security
- **Biometric Authentication:** Lock & unlock the app via device Fingerprint / Face ID (`capacitor-native-biometric`).
- **Role Permissions:** Restrict staff/salesman access from viewing profit margins, editing stock, or altering settings.

### 8. 🌐 Bilingual (English & Urdu Nastaliq)
- Full localized interface with custom **Jameel Noori Nastaleeq** & **Noto Nastaliq** typography for native Urdu readability.

---

## 🏗️ Technical Architecture & Stack

| Layer | Technologies Used |
|---|---|
| **Frontend Framework** | React 19, Vite 8, JavaScript (ESNext) |
| **Mobile Bridge / Native** | Capacitor 7 (Camera, Biometrics, Filesystem, Haptics, Local Notifications) |
| **Styling & UI System** | Custom Glassmorphism UI, Framer Motion transitions |
| **Backend & Cloud Sync** | Supabase (PostgreSQL), Cloud Auth, Real-time Sync |
| **Document Generation** | jsPDF (Thermal & A4 bills), SheetJS / XLSX (Excel reports) |
| **Hardware & Scanning** | @zxing/library, @capacitor-community/barcode-scanner |

---

## 👨‍💻 Developer & Contact

Developed by **Awais Khan**  
- **GitHub:** [@awaiskhans4039-cpu](https://github.com/awaiskhans4039-cpu)  
- **LinkedIn:** *[Add Your LinkedIn Profile Link Here]*  

*Interested in a live demonstration, custom feature implementation, or licensing this software for your retail business? Feel free to connect via LinkedIn or open an issue!*

---

## ⚖️ Intellectual Property
© 2026 Awais Khan. All rights reserved.  
Unauthorized copying, modification, distribution, or reverse engineering of this software is strictly prohibited.
