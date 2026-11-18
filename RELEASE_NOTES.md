# 🚀 CellFlow Android Release Notes — Version 3.5.1

**Release Tag:** `v3.5.1-production`  
**Target Platform:** Android (Smartphones & Tablets)  
**APK Build:** `cellflow v3.5.1.apk`  
**Direct Download:** [Download CellFlow v3.5.1 APK](https://txhcdtownkvydrdxlmjd.supabase.co/storage/v1/object/public/App_release/cellflow%20v3.5.1.apk)  
**Official Portal:** [cellflow.shop](https://cellflow.shop)  

---

## 🌟 Executive Summary

**CellFlow v3.5.1** delivers a major **UI & usability overhaul**, **press-and-hold bilingual metric guides** in pure English and Urdu, **automated mobile layout overflow fixes**, and comprehensive **security hardening** — including **brute-force PIN rate limiting with salted PBKDF2 cryptography**, **zero-leak scoped salesman authentication**, **Android OS backup extraction blocking**, and **`SHA-256` verified live OTA update support**.

---

## ✨ 1. New Features & UI Improvements

* **💡 Press & Hold Metric Guides (English & Urdu):**
  * Long-press any summary card across **Dashboard, Inventory, Khata Book, Products, Payments, and Sales History** to inspect exact metric meanings and calculation logic in your active app language (pure English or Urdu script).
* **📊 Smart Month-over-Month Dashboard Insights:**
  * Restored the Dashboard comparison pill alongside True Net Profit and Revenue, showing all positive growth and mild dips down to `-10%` while hiding steep mid-month fluctuations.
* **🎨 Redesigned System Settings, Inventory & Khata UI:**
  * Upgraded Settings Drawer layout, refreshed Inventory Analytics and Khata Ledger screens, enhanced the interactive login mascot, and expanded Urdu translations across the app.
* **📱 Responsive Mobile Screen Fit & Overflow Guards:**
  * Fixed horizontal overflow on narrow mobile screens (such as New Sale Quick Pick cards), reinforced CSS grid shrink boundaries, and added automated layout overflow verification checks.
* **🔍 Enhanced Salesman Audit & Repair Tracking:**
  * Salesman product edit audit logs now show structured old-vs-new diffs (stock & pricing changes), paired with clean `TKxxxxxx` repair ticket tracking at `track.cellflow.shop`.
* **⚡ Live OTA Update Readiness:**
  * Integrated seamless in-app OTA bundle architecture with offline caching so future minor updates can deploy cleanly without reinstalling APKs.

---

## 🔒 2. Security & Privacy Enhancements

* **🔐 Brute-Force PIN Lockout & PBKDF2 Cryptography:**
  * Added progressive rate limiting (`5s` up to `5 min` lockout) on failed `LockedScreen` PIN attempts, backed by `120,000`-iteration salted **PBKDF2** hashing and timing-safe verification.
* **🛡️ Scoped Salesman Pairing & Admin Lock Guard:**
  * Paired salesman devices authenticate with isolated scoped credentials instead of sharing Admin JWT session tokens, include guardrails preventing an Admin phone from switching itself into Salesman Mode, and perform automatic rollback on pairing errors.
* **🧱 Strict Multi-Tenant Row-Level Security (`RLS`):**
  * Enforced PostgreSQL RLS isolation policies across tenant tables so every shop's invoices, inventory, Khata ledgers, and customer accounts remain strictly isolated.
* **📦 Android Data Backup Extraction Disabled:**
  * Configured `android:allowBackup="false"` and `android:fullBackupContent="false"` in `AndroidManifest.xml` to block unauthorized ADB/cloud backup extraction of local shop data.
* **🔑 `SHA-256` Update Verification & Hardened Repair Tracking:**
  * Live OTA bundles validate against `SHA-256` checksums before activation, Bluetooth printer discovery filters non-printer devices, and public repair lookup routes enforce tightened security policies.

---

## 📲 How to Update

1. Download the latest APK:  
   👉 [cellflow v3.5.1.apk (Direct Download)](https://txhcdtownkvydrdxlmjd.supabase.co/storage/v1/object/public/App_release/cellflow%20v3.5.1.apk)
2. Open the downloaded file on your Android phone and select **Update / Install**.
3. All existing shop stock, Khata ledgers, and repair tickets remain **100% intact and automatically preserved**.

---
*Developed by Awais Khan (AK Softech) · [support@cellflow.shop](mailto:support@cellflow.shop) · [cellflow.shop](https://cellflow.shop)*
