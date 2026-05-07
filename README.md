# 🥛 Milk Passbook - Professional Dairy Management

[![Kotlin](https://img.shields.io/badge/Kotlin-1.9.24-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)](https://kotlinlang.org/)
[![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-2024.12.01-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white)](https://developer.android.com/jetpack/compose)
[![Material 3](https://img.shields.io/badge/Material_3-Modern_UI-757575?style=for-the-badge&logo=materialdesign&logoColor=white)](https://m3.material.io/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

**Milk Passbook** is a precision-engineered Android application designed for dairy farmers to transform their traditional paper ledger into a high-performance digital ecosystem. Built with a focus on data integrity, visual intelligence, and local usability, it empowers farmers to track, analyze, and manage their milk production with professional-grade tools.

---

## 💎 Premium Features & Logic

### 📊 Visual Intelligence & Analytics
- **Privacy-First & Offline**: Zero internet permissions required. Your data never leaves your device except when you explicitly export or backup.
- **Dynamic Trend Analysis**: Powered by the **Vico Charting Engine**, providing real-time visualizations of Weight, FAT, SNF, and Income trends across Weekly, Monthly, and 6-Month windows.
- **Aggregated Financial Stats**: Sophisticated SQL-level calculations for Lifetime Average Rate, Potential Revenue, and Actual Received Cash.
- **Custom Range Reporting**: Real-time stats calculation for any selected date range, including total production and revenue metrics.

### 📄 Intelligent Export System
- **Professional PDF Reports**: Generates A4-compliant PDF reports for milk slips, including high-quality embedded receipt images, professional typography (DairyBlue theme), and automatic multi-page pagination.
- **Excel-Compatible CSV**: Lightweight export using **UTF-8 BOM** for perfect compatibility with Microsoft Excel (ensuring Tamil text renders correctly). Includes a high-level analytics block (totals and averages) appended to every export.
- **Automatic Storage Management**: Integrated cleanup services that automatically purge old export files to keep device storage clean.

### 🛡️ Data Integrity & Security
- **Versioned Backups**: JSON-based backup system with internal versioning to prevent data corruption during schema migrations.
- **Transaction-Safe Imports**: All data restores are wrapped in Room transactions, ensuring "all-or-nothing" safety during critical data operations.
- **Duplicate Prevention**: Intelligent logic prevents redundant entries by checking Date + Shift combinations during import.

### 🌍 Localized Excellence
- **Dual Language Support**: Seamless, real-time switching between **English** and **Tamil (தமிழ்)**.
- **Localized Calendar Logic**: Specialized wrapping for Material 3 DatePickers to ensure month names and dates respect the user's selected language.
- **Timezone Normalization**: Advanced UTC-to-Local-Midnight normalization ensures data consistency across different device time settings.

---

## 🛠️ Technical Architecture

The application adheres to **Clean Architecture** principles with a reactive **MVVM** pattern:

- **UI Layer**: Jetpack Compose with Material 3 components. Uses `StateFlow` and `collectAsStateWithLifecycle` for efficient, lifecycle-aware UI updates.
- **Domain/Data Layer**: 
    - **Room Persistence**: Optimized with indices for fast date-based lookups and sophisticated SQL aggregations.
    - **Repository Pattern**: Centralizes data access logic and provides a clean API to ViewModels.
- **Dependency Injection**: **Hilt** provides scoped dependencies, ensuring a decoupled and testable codebase.
- **Services**: Dedicated singleton services for PDF Generation, CSV Export, and Data Backup logic.

---

## 📸 Interface Design

The app features a **"Glassmorphism-Lite"** design system using custom components:

| Dashboard | Analytics | Receipt Management |
| :---: | :---: | :---: |
| ![Home](https://via.placeholder.com/200x400?text=Dashboard) | ![Analytics](https://via.placeholder.com/200x400?text=Analytics) | ![Slips](https://via.placeholder.com/200x400?text=Slips) |

- **DairyBlue Theme**: A professional, calming palette designed for readability and focus.
- **Shift Visuals**: Intuitive Sun/Moon iconography for Morning and Evening shifts.
- **Responsive Layouts**: Optimized for various screen sizes with fluid components.

---

## 🚀 Development Setup

### Prerequisites
- Android Studio Ladybug+
- JDK 17
- Android API 26+ (Oreo)

### Build
```bash
./gradlew assembleDebug
```

---

## 🗺️ Roadmap
- [ ] **Cloud Sync**: Optional Google Drive integration for cross-device backup.
- [ ] **OCR Engine**: AI-powered receipt scanning to automatically extract amounts and dates from photos.
- [ ] **Multi-Farmer Support**: Manage multiple accounts or farms within a single app.

---

## 📄 License
Distributed under the **MIT License**. See `LICENSE` for more information.

---

**Developed with ❤️ for the farming community by The Man SARMO.**
