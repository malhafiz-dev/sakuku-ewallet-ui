# 📱 Sakuku - E-Wallet Mobile Web Application UI

A modern, responsive, and accessible mobile-first E-Wallet Web Application UI template built with **Tailwind CSS v4** and **HTML5**.

![Tailwind CSS v4](https://img.shields.io/badge/Tailwind_CSS-v4.0-38BDF8?style=for-the-badge&logo=tailwindcss)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![Iconify](https://img.shields.io/badge/Iconify-1769AA?style=for-the-badge&logo=iconify&logoColor=white)
![Accessibility](https://img.shields.io/badge/Accessibility-WCAG_Compliant-2E7D32?style=for-the-badge)

---

## 🌟 Key Features

- **Mobile-First Responsive Layout**: Centered container layout (`mx-auto max-w-3xl`) optimized for mobile devices while maintaining an elegant presentation on desktop and tablet viewports.
- **Consistent Brand Blue Design System**: Custom HSL/Hex color tokens (`#0D47A1` & `#1565C0`) paired with smooth hover states and accessible focus rings (`focus:ring-blue-400`).
- **Comprehensive UI Screens**:
  - **Splash Screen** (`pages/index.html`)
  - **Interactive Dashboard** (`pages/dashboard.html`) with balance visibility toggle and modular transaction modals
  - **User Onboarding** (`pages/register.html`, `pages/register-pin.html`)
  - **Transaction History** (`pages/transaction-history.html`) with search input and category badges
  - **Withdrawal Flow** (`pages/withdrawal.html`)
  - **Account & Settings** (`pages/account.html`, `pages/account-settings.html`)
  - **Transaction Status Pages** (*Settled*, *Pending*, *Failed*, *Expired*, *Canceled*)
- **Accessibility & UX**: Fully compliant with `axe-linter` rules (`lang="id"`, `aria-label` attributes on icon-only interactive controls, discernible contrast ratios).

---

## 🛠️ Tech Stack & Tooling

- **HTML5**: Semantic markup hierarchy.
- **Tailwind CSS v4**: Built using the official `@tailwindcss/cli` compiler.
- **Iconify Tailwind Plugin**: Scalable vector icons powered by `@iconify/tailwind4`.
- **BrowserSync**: High-performance local development server with hot-reloading.
- **Prettier & Tailwind Plugin**: Automated code formatting.

---

## 📁 Directory Structure

```text
aplikasi-e-wallet/
├── dist/                      # Production-ready compiled assets & pages
│   ├── assets/
│   │   ├── css/main.css       # Compiled Tailwind CSS bundle
│   │   ├── images/            # Graphics, badges, and illustrations
│   │   └── js/main.js         # Interactive UI logic & modal scripts
│   ├── pages/                 # Application screen views
│   │   ├── account.html
│   │   ├── account-settings.html
│   │   ├── dashboard.html
│   │   ├── index.html (Splash)
│   │   ├── register.html
│   │   ├── register-pin.html
│   │   ├── transaction-canceled.html
│   │   ├── transaction-expired.html
│   │   ├── transaction-failed.html
│   │   ├── transaction-history.html
│   │   ├── transaction-pending.html
│   │   ├── transaction-settled.html
│   │   └── withdrawal.html
│   └── index.html             # Component design showcase page
├── src/
│   └── input.css              # Tailwind CSS entrypoint & custom color variables
├── package.json
├── .gitignore
├── .prettierrc
└── README.md
```

---

## 🚀 Getting Started

### 1. Prerequisites
Ensure you have [Node.js](https://nodejs.org/) installed (v18.0.0 or higher recommended).

### 2. Clone & Install Dependencies
```bash
# Clone repository
git clone https://github.com/your-username/sakuku-ewallet-ui.git

# Navigate to project root
cd sakuku-ewallet-ui

# Install dependencies
npm install
```

### 3. Start Development Server
```bash
npm run dev
```
Launches a BrowserSync dev server at `http://localhost:3000` with live reload on file modifications.

### 4. Build for Production
```bash
npm run build
```
Compiles and minifies the final CSS bundle to `dist/assets/css/main.css`.

---

## 🎯 Purpose & Acknowledgments

This repository was created as a **hands-on learning project** to practice and showcase proficiency in **Tailwind CSS v4**, modern CSS layout techniques, and responsive web design. Built as part of a Web Development Course completion portfolio.
