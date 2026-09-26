# 📱 Stockify — Smart Mobile Shop POS & ERP System

[![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20Web-green.svg)](https://capacitorjs.com/)
[![Version](https://img.shields.io/badge/Version-v3.4.5-orange.svg)](https://github.com/awaiskhans4039-cpu/Stockify-app-public-repository)
[![React](https://img.shields.io/badge/React-19.x-blue.svg?logo=react)](https://react.dev/)
[![Capacitor](https://img.shields.io/badge/Capacitor-7.x-119EFF.svg?logo=capacitor)](https://capacitorjs.com/)
[![Backend](https://img.shields.io/badge/Backend-Supabase%20PostgreSQL-3ECF8E.svg?logo=supabase)](https://supabase.io/)
[![Design](https://img.shields.io/badge/Design-Glassmorphism%20%26%20Framer%20Motion-FF69B4.svg)](https://framer.com/motion)
[![License](https://img.shields.io/badge/License-Proprietary%20%2F%20Closed--Source-red.svg)](#-intellectual-property--license)

> 🔒 **Proprietary Software Notice:**  
> **Stockify** is an enterprise commercial software solution built specifically for mobile phone shops, gadget retailers, and electronics repair businesses. The core production source code is maintained in a private repository. This repository serves as the **official public showcase, architectural documentation, and APK release portal**.

---

## 📲 Download & Test Android APK

Experience the speed and capabilities of **Stockify** directly on your Android phone:

📥 **[Download Latest Stockify Android APK (v3.4.5 / 3.4.4)](https://txhcdtownkvydrdxlmjd.supabase.co/storage/v1/object/public/App_release/Stockify%20version%203.4.4.apk)**  

> 💡 **Installation Tip:** When installing the APK on your Android device, allow *"Install from Unknown Sources"* if prompted by your browser or file manager.

---

## 🌟 About Stockify

Managing a mobile retail business involves tracking high-value devices by **unique IMEI numbers**, organizing hundreds of accessories, maintaining **customer credit ledgers (Khata / Udhaar)**, tracking **repair job cards**, managing **installments (EMI)**, and complying with legal documentation when purchasing used phones.

**Stockify** is an all-in-one digital operating system engineered to replace paper registers, fragmented spreadsheets, and clunky legacy desktop POS systems with a sleek, lightning-fast, mobile-first experience.

---

## 🚀 Key Modules & Capabilities

### 1. 🛒 Point of Sale (POS) & Rapid Billing
- **Instant Product Search:** Query inventory in milliseconds by product title, brand, barcode, or IMEI.
- **Hardware & Camera Barcode Scanning:** Powered by native camera scanning (@zxing/library) and external barcode guns with audio and haptic feedback.
- **Multi-Payment Support:** Seamlessly record transactions via Cash, EasyPaisa, JazzCash, Bank Transfer, or Khata (Udhaar).
- **Thermal & PDF Invoicing:** Generate professional thermal slips and digital invoices with instant one-click sharing on WhatsApp.

### 2. 📦 Dual-Category Inventory Control
- **IMEI & Serial Handset Engine:** Dedicated tracking for IMEI-bound smartphones with unique warranty and condition records.
- **Accessory Stock Management:** Quantity-based inventory with real-time cost, retail price, and automated profit margin calculations.
- **Live Depletion Alerts:** Immediate visual warnings when product quantities drop below custom safety thresholds.
- **Stock Inward Batches:** Complete tracking of incoming vendor shipments, supplier balances, and purchase invoices.

### 3. 📒 Digital Khata (Customer Ledger & Udhaar Book)
- **Customer Profiles:** Comprehensive debit/credit balances for walk-in shoppers, regular customers, and wholesale dealers.
- **Atomic Jama / Naam Tracking:** Time-stamped history of customer credits, repayments, balance adjustments, and discount logs.
- **Account Statements:** Export branded PDF account statements for instant WhatsApp payment reminders.

### 4. 🔧 Mobile Repair Service Desk
- **Job Ticketing & Claim Slips:** Issue repair tickets with customer info, device passcode, physical condition, and diagnosis.
- **Lifecycle Tracking:** Step-by-step repair status progression (*Received ➔ Inspecting ➔ Fixed ➔ Delivered*).
- **Advance & Final Billing:** Collect advance repair deposits with automatic ledger synchronization upon job delivery.

### 5. 📱 Used Phone Registration & Verification
- **Seller Identity Verification:** Capture seller CNIC number, contact details, device IMEI, and physical photo.
- **Legal Purchase Agreements:** Digital verification slips protecting shopkeepers from illicit or stolen handsets.

### 6. 📅 Installment (EMI) Management
- **Custom Financing Plans:** Define custom down-payments, monthly installment tenures, and profit markups.
- **Payment Schedule Tracker:** Real-time visibility into paid, upcoming, and overdue installments.

### 7. 📊 Profit Overview & Financial Analytics
- **Live Profit Engine:** Instant tracking of daily net profit, monthly gross profit, and operating expenses.
- **Interactive Visualizations:** Dynamic 7-day, 14-day, and 30-day Bar & Line charts powered by date-normalized analytics.
- **Performance Metrics:** Real-time insights into top-selling products and highest-margin categories.

### 8. 🛡️ Security, Biometrics & Staff Permissions
- **Biometric Authentication:** Unlock the application using device Fingerprint or Face ID via `capacitor-native-biometric`.
- **Salesman Protection Mode:** Restrict staff from viewing wholesale cost prices, profit margins, reports, or shop settings.
- **Auto-Lock Security:** Configurable idle timeout lock with master PIN fallback.

### 9. 🌐 Bilingual (English & Urdu Nastaliq)
- Full localized interface with authentic **Jameel Noori Nastaleeq** & **Noto Nastaliq** typography for native Urdu readability.
- Fluid glassmorphic UI with backdrop blur filters, smooth Framer Motion transitions, and Dark/Light responsive accents.

---

## 🏗️ Technical Architecture & Database Design

Stockify is engineered on a **Local-First, Cloud-Synced Architecture** to ensure zero downtime and uninterrupted sales even in offline environments.

```text
[ React 19 Frontend + Glassmorphic UI ]
               │
               ▼
[ DatabaseService.js (Local Storage Cache + Normalization) ]
               │
       ┌───────┴───────┐
       ▼               ▼
[ Local Cache ]   [ Supabase PostgreSQL Cloud ]
(Instant Offline)  ├── Atomic Stored Procedures (RPC)
                   │   ├── record_sale_transaction
                   │   ├── reverse_sale_transaction
                   │   ├── record_khata_payment
                   │   ├── receive_repair_job
                   │   └── deliver_repair_job
                   ├── Row Level Security (RLS)
                   └── Real-time Indexing
```

### Enterprise Stored Procedures (`supabase_schema.sql`):
1. **`record_sale_transaction`**: Atomic multi-item sale, stock deduction, sale recording, customer ledger (Khata) update, and salesman commissions.
2. **`reverse_sale_transaction`**: Atomic sale rollback, stock restoration, customer balance reversal, and khata log removal.
3. **`record_khata_payment`**: Atomic payment receipt, customer balance adjustment, and ledger entry creation.
4. **`receive_repair_job`**: Atomic repair card creation, status initialization, and upfront deposit ledger entry.
5. **`deliver_repair_job`**: Atomic repair completion, final billing, and routing unpaid balances to customer khata.

---

## 💻 Tech Stack Overview

| Layer | Technologies Used |
|---|---|
| **Frontend Framework** | React 19, Vite 8, Modern ESNext JavaScript |
| **Mobile Runtime** | Capacitor 7 (Android Native Plugins) |
| **Styling & Motion** | Custom Glassmorphic CSS, Framer Motion |
| **Database & Cloud Backend** | Supabase (PostgreSQL 15+ with Atomic Stored Procedures) |
| **Data Sync Engine** | Local-First Service Layer (`DatabaseService.js`) with Offline Fallback |
| **Hardware Integration** | Camera Scanner (@zxing/library), Biometrics, Haptics |
| **Document Generation** | jsPDF (Thermal & A4 bills), SheetJS / XLSX (Excel reports) |
| **Typography** | Noto Nastaliq Urdu, Jameel Noori Nastaleeq, Inter |

---

## 👨‍💻 Developer & Inquiries

Developed by **Awais Khan**  
- **GitHub:** [@awaiskhans4039-cpu](https://github.com/awaiskhans4039-cpu)  
- **Project Showcase:** [Stockify-app-public-repository](https://github.com/awaiskhans4039-cpu/Stockify-app-public-repository)  

*Interested in a live demonstration, commercial licensing, custom feature implementation, or white-label solutions for your retail business? Feel free to reach out via GitHub or open an issue!*

---

## 📄 Intellectual Property & License
© 2026 Awais Khan. All rights reserved.  
Stockify is proprietary commercial software. Unauthorized copying, distribution, modification, public display, or reverse engineering of any portion of this software is strictly prohibited.