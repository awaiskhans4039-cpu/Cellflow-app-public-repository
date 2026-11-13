# 🚀 CellFlow Android Release Notes — Version 3.4.8

**Release Tag:** `v3.4.8-production`  
**Target Platform:** Android (Smartphones & Tablets)  
**APK Build:** `CellFlow V3.4.8.apk`  
**Direct Download:** [Download CellFlow v3.4.8 APK](https://txhcdtownkvydrdxlmjd.supabase.co/storage/v1/object/public/App_release/CellFlow%20V3.4.8.apk)  
**Official Portal:** [cellflow.shop](https://cellflow.shop)  

---

## 🌟 Executive Summary

**CellFlow v3.4.8** brings high-priority stability improvements to **Salesman Mode real-time syncing**, eliminates offline queue race conditions, resolves edge-case calculation bugs in customer Khata balances, and enforces stricter Pakistani telecom & CNIC validation standards across POS billing and repair ticketing.

---

## ⚡ 1. Salesman Mode & Multi-Device Sync Enhancements

* **🔄 Bulletproof Salesman Real-Time Sync:**
  * Fixed an issue where staff device permissions lagged after changing screen access toggles on the Admin phone. Permission updates now stream instantly over active WebSockets.
  * Offline activity queue now guarantees ordered delivery: if a salesman records billing, Khata entries, or repairs in a basement market without internet, all actions sync in exact chronological order the moment connectivity resumes.
* **📷 Instant Passwordless QR Pairing:**
  * Optimized 10-minute expiring encrypted QR pairing to ensure faster device authorization without triggering unnecessary PIN or biometric lockout prompts on staff devices.
* **🙈 Wholesale Cost & Profit Shielding:**
  * Enforced global purchase price hiding across POS search, product lists, and quick-bill popups on salesman devices, preventing counter customers or staff from viewing wholesale margins.
* **🛡️ Deletion & Anti-Tamper Guard:**
  * Strictly prevented salesman devices from deleting invoices, modifying historical EMI schedules, or clearing ledger records without master admin override.

---

## 🐛 2. Critical Bug Fixes & Stability

* **📱 Phone Number & WhatsApp Link Normalization:**
  * Standardized Pakistani mobile numbers (`03XX-XXXXXXX` / `+923XXXXXXXXX`) with auto-cleansing. One-tap WhatsApp receipt sharing and payment reminders now reliably open WhatsApp without "Invalid Phone Number" errors.
* **🪪 CNIC 15-Character Strict Format:**
  * Added auto-formatting and character limits to seller and customer CNIC inputs (`XXXXX-XXXXXXX-X`) for dual IMEI purchases and recovery tracking.
* **👤 User Profile & Avatar Relogin Fix:**
  * Resolved a bug where logging out and re-logging in could display a broken `null` avatar placeholder; added direct photo removal and default monogram initials fallback.
* **🖨️ Bluetooth Thermal Printing Reconnection:**
  * Fixed auto-reconnect drops on 58mm and 80mm ESC/POS Bluetooth thermal printers after Android screen timeout.
* **🔧 Live Repair Customer Link Fix:**
  * Cleaned up redundant UI pills on repair tickets and streamlined customer tracking direct integration with `https://track.cellflow.shop/{ticketId}`.
* **💰 Khata & EMI Ledger Calculation Guard:**
  * Resolved an edge-case rounding discrepancy when calculating partial advance down payments on 9-month and 12-month installment schedules.

---

## 🔒 3. Data Integrity & Security

* **100% Safe Cloud Sync Engine:**
  * Guaranteed zero data loss with local SQLite/IndexedDB caching combined with auto-resilient background sync to Supabase PostgreSQL.
* **Remote Session Kill Switch:**
  * Shop owners can revoke any paired salesman session in 1 tap from their Admin phone; the staff device immediately resets to the scan screen.

---

## 📲 How to Update

1. Download the latest APK:  
   👉 [CellFlow V3.4.8.apk (Direct Download)](https://txhcdtownkvydrdxlmjd.supabase.co/storage/v1/object/public/App_release/CellFlow%20V3.4.8.apk)
2. Open the downloaded file on your Android phone and select **Update / Install**.
3. All existing shop stock, Khata ledgers, and repair tickets will remain **100% intact and automatically upgraded**.

---
*Developed by Awais Khan (AK Softech) · [support@cellflow.shop](mailto:support@cellflow.shop) · [cellflow.shop](https://cellflow.shop)*
