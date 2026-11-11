# 📱 CellFlow — Smart Mobile Shop POS, Khata & ERP System

[![Website](https://img.shields.io/badge/Website-cellflow.shop-0ea5e9.svg)](https://cellflow.shop)
[![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20Web-10b981.svg)](https://capacitorjs.com/)
[![Version](https://img.shields.io/badge/Version-v3.4.8-2563eb.svg)](https://github.com/awaiskhans4039-cpu/Cellflow-app-public-repository)
[![React](https://img.shields.io/badge/React-19.x-38bdf8.svg?logo=react)](https://react.dev/)
[![Capacitor](https://img.shields.io/badge/Capacitor-7.x-119EFF.svg?logo=capacitor)](https://capacitorjs.com/)
[![Backend](https://img.shields.io/badge/Backend-Supabase%20PostgreSQL%20%26%20Realtime-3ECF8E.svg?logo=supabase)](https://supabase.com/)
[![License](https://img.shields.io/badge/License-Proprietary%20%2F%20Closed--Source-dc2626.svg)](#-intellectual-property--license)

> 🔒 **Proprietary Commercial Software Notice:**  
> **CellFlow** ([cellflow.shop](https://cellflow.shop)) is an enterprise commercial POS and business management platform engineered specifically for mobile phone shops, gadget retailers, and electronics repair centers. Core production source code is maintained privately. This repository serves as the **official public product showcase, architectural overview, and release portal**.

---

## 📲 Download & Experience Android APK

Test the speed, offline reliability, and real-time multi-device sync of **CellFlow** directly on your Android smartphone:

📥 **[Download Latest CellFlow Android APK](https://txhcdtownkvydrdxlmjd.supabase.co/storage/v1/object/public/App_release/Stockify%20version%203.4.4.apk)**  

> 💡 **Installation Tip:** Allow *"Install from Unknown Sources"* if prompted by your browser or Android file manager.

---

## 🌟 About CellFlow

Running a modern mobile retail and repair business requires precision across **unique IMEI-tracked handsets**, hundreds of accessories, **customer credit ledgers (Khata / Udhaar)**, **installment financing (EMI)**, **repair service jobs**, and **used-device identity verification**.

**CellFlow** replaces paper registers, fragmented spreadsheets, and legacy desktop software with a sleek, mobile-first, **offline-capable POS operating system** featuring real-time synchronization between **Owner (Admin)** and **Staff (Salesman)** phones.

---

## 🔥 Flagship Feature: Enterprise Salesman Mode & Zero-Trust Counter Control

One of CellFlow's standout breakthroughs is **Salesman Mode** — purpose-built for shop owners who want staff managing counter sales on a second device **without ever exposing wholesale profits, business secrets, or risking data manipulation**.

* **📷 1-Scan Passwordless QR Pairing:** Connect a salesman's phone in seconds by scanning a **10-minute expiring encrypted QR code** generated on the Admin phone. Staff access the counter immediately without ever knowing the owner's email, password, or OTP — and without forced pin/biometric lockouts upon pairing.
* **🙈 Wholesale Cost & Profit Privacy:** Automatically conceals purchase/cost prices, net profit margins, supplier totals, shop expenses, and 12-month financial analytics from staff devices.
* **🛡️ 13 Granular Micro-Action Guards & 9 Module Controls:**
  * **Loss-Sale Prevention:** Blocks staff from billing products below wholesale cost.
  * **Anti-Tampering Controls:** Restricts invoice deletions, EMI payment reversals, EMI plan edits, Khata record deletions, unauthorized stock edits, and bulk database exports.
  * **Per-Device Screen Access:** Toggle individual tabs (*Dashboard, New Sale, Products, Repairs, History, Khata, Payments, EMI, Inventory*) dynamically per device.
* **📡 Real-Time Staff Activity Audit Trail:** Automatically captures every counter sale, Khata collection, EMI reversal, and repair action tagged with **Salesman Name, Device Model, Severity, and Timestamp** — including offline queuing so no event is ever missed.
* **⚡ Live Permission Updates & 1-Tap Kill Switch:** Adjust staff permissions live over WebSockets, stamp the active salesman's identity onto receipts, or **instantly revoke & remotely wipe** any paired device if an employee leaves or a phone is lost.

| Counter Security Layer | Protection Provided to the Business Owner |
|---|---|
| **Device Onboarding** | Time-limited QR pairing; zero owner credentials ever shared |
| **Margin Confidentiality** | Wholesale cost prices, expenses & net profit reports hidden completely |
| **Counter Integrity** | Prevents below-cost billing, silent invoice deletions, & Khata/EMI tampering |
| **Remote Oversight** | Live activity feed synced from staff devices to the Admin phone |
| **Session Command & Control** | Single active Admin enforcement + 1-tap remote logout & cache wipe |

---

## 🚀 Complete Business Modules

### 1. 🛒 Smart POS, Rapid Billing & Bluetooth Thermal Printing
- **Instant IMEI & Product Search:** Filter handsets and accessories in milliseconds by brand, title, barcode, or unique IMEI.
- **Native Camera & Gun Scanner Support:** Built-in barcode/QR/IMEI camera scanning alongside external USB/Bluetooth barcode scanners with audio & haptic confirmation.
- **Multi-Mode Split Payments:** Accept Cash, EasyPaisa, JazzCash, Bank Transfer, or Customer Khata (Udhaar).
- **Dual-Engine ESC/POS Thermal Printing:** Direct native Android Bluetooth SPP and Web BLE receipt printing for `58mm` and `80mm` printers, plus branded PDF invoices and 1-tap WhatsApp delivery.

### 2. 📦 Dual-Category Inventory & Supplier Batches
- **IMEI & Serial Handset Tracking:** Per-device unit records with multi-device **duplicate-IMEI overselling detection**.
- **Accessory Stock & Depletion Alerts:** Automated low-stock visual warnings and real-time margin tracking.
- **Supplier Purchases & Excel Export:** Track inward stock batches, vendor balances, and export stock sheets to `.xlsx`.

### 3. 📒 Digital Khata (Customer Udhaar & Ledger)
- **Zero-Duplicate Multi-Device Settlement:** Atomic **"Mark as Paid"** linking ensures Admin and Salesman devices display identical "Paid" badges and net balances in real time without ghost entries.
- **Payment Reminders & PDF Statements:** Schedule due reminders and send branded ledger statements over WhatsApp.

### 4. 📅 Deterministic Installment (EMI) Management
- **Custom Financing Plans:** Configure down payments, profit markups, and daily, weekly, or monthly installment schedules.
- **Real-Time Multi-Device Reversals:** Centralized financial calculation guarantees 100% consistent paid counts, skipped installments, reversals, and remaining balances across all synced devices.

### 5. 🔧 Mobile Repair Desk & Used Phone Verification
- **Repair Job Cards & Lifecycle Tracking:** Track repairs through *Received ➔ In Progress ➔ Completed ➔ Delivered*, including advance deposits and spare-part inventory deduction.
- **Used Handset Seller Verification:** Record seller CNIC, phone details, IMEI, and photos to generate proof-of-purchase slips protecting shops against stolen devices.

### 6. 🌐 Bilingual English & Urdu (Nastaliq) Experience
- Native support for **English** and **Urdu** with bundled *Jameel Noori Nastaleeq* & *Noto Nastaliq* typography, Dark/Light themes, and responsive mobile-first layouts across all screen widths.

---

## 🏗️ Enterprise Sync & Reliability Architecture

CellFlow uses a **Local-First, Cloud-Authoritative Delta** architecture engineered for zero counter downtime, low data egress, and conflict-free multi-device operation:

```text
  [ Mobile / Web POS UI (React 19 + Framer Motion) ]
                           │
                           ▼
  [ Local-First Sync Layer + Edge Clock Offset ] ◄── Server Time Sync
          │                              │
          ▼                              ▼
  [ Offline Local Cache ]       [ Supabase Cloud Backend ]
  (Instant 0ms Counter UX)       ├── Granular Single-Record Realtime Deltas
                                 ├── Zero-Echo Ping-Pong Loop Suppression
                                 ├── Row-Level Security & Anti-Spoof Guards
                                 ├── ACID Transactional Stored Procedures (RPC)
                                 └── Encrypted .shopbak Disaster-Recovery Backups
```

### Key Architectural Guarantees:
- **Zero-Echo Realtime Delta Engine:** Synchronizes single-row database changes instantaneously across connected devices while suppressing local write echoes to eliminate sync loops and unnecessary database egress.
- **Automatic Edge Server Time-Drift Correction:** Measures clock skew against authoritative server time via zero-cost HTTP headers, ensuring chronological accuracy and clean conflict resolution even if a device clock is misconfigured.
- **ACID-Compliant Database Procedures:** Multi-step sales, reversals, Khata settlements, and repair deliveries execute atomically inside PostgreSQL transactions, preventing partial writes or stock mismatches.
- **Encrypted Backups:** Scheduled daily `.shopbak` local archives and encrypted cloud restoration flows.

---

## 💻 Technology Stack

| Layer | Technologies |
|---|---|
| **Frontend & UI** | React 19, Vite 8, Custom Glassmorphic CSS, Framer Motion, Recharts |
| **Mobile Runtime** | Capacitor 7 (Camera, Filesystem, Contacts, Biometrics, Notifications) |
| **Database & Sync** | Supabase (PostgreSQL, Row-Level Security, Stored Procedures, Realtime WebSockets) |
| **Hardware & Printing** | Android Classic Bluetooth SPP & Web BLE ESC/POS, `@zxing/library` Scanner |
| **Export & Documents** | jsPDF (Receipts & Statements), SheetJS / XLSX, JSZip, Tesseract OCR |
| **Typography** | Noto Nastaliq Urdu, Jameel Noori Nastaleeq, Inter |

---

## 👨‍💻 Developer, Official Website & Commercial Inquiries

Developed by **Awais Khan**

- 🌐 **Official Website:** [https://cellflow.shop](https://cellflow.shop)
- ✉️ **Business & Support Email:** [support@cellflow.shop](mailto:support@cellflow.shop)
- 💻 **GitHub:** [@awaiskhans4039-cpu](https://github.com/awaiskhans4039-cpu)
- 📂 **Public Showcase:** [Cellflow-app-public-repository](https://github.com/awaiskhans4039-cpu/Cellflow-app-public-repository)

*Interested in a live product demo, commercial store license, custom enterprise features, or white-label deployment for your mobile retail business? Reach out via email at **support@cellflow.shop** or open an inquiry!*

---

## 📄 Intellectual Property & License

© 2026 Awais Khan / CellFlow. All rights reserved.  
**CellFlow** is proprietary closed-source commercial software. Unauthorized copying, redistribution, modification, public re-hosting, or reverse engineering of any component of this software is strictly prohibited.
