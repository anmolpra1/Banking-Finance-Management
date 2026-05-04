<div align="center">
  <br />
  <h1>💳 Banking Finance Management</h1>
  <p>A full-stack financial SaaS platform built with Next.js — connect multiple bank accounts, track transactions in real-time, and transfer funds seamlessly.</p>

  <div>
    <img src="https://img.shields.io/badge/-Next_JS-black?style=for-the-badge&logoColor=white&logo=nextdotjs&color=000000" alt="nextdotjs" />
    <img src="https://img.shields.io/badge/-TypeScript-black?style=for-the-badge&logoColor=white&logo=typescript&color=3178C6" alt="typescript" />
    <img src="https://img.shields.io/badge/-Tailwind_CSS-black?style=for-the-badge&logoColor=white&logo=tailwindcss&color=06B6D4" alt="tailwindcss" />
    <img src="https://img.shields.io/badge/-Appwrite-black?style=for-the-badge&logoColor=white&logo=appwrite&color=FD366E" alt="appwrite" />
  </div>

  <br />

  <a href="https://github.com/anmolpra1/Banking-Finance-Management">
    <img src="https://img.shields.io/github/stars/anmolpra1/Banking-Finance-Management?style=social" alt="stars" />
  </a>
</div>

---

## 📋 Table of Contents

1. [Overview](#overview)
2. [Tech Stack](#tech-stack)
3. [Features](#features)
4. [Getting Started](#getting-started)
5. [Environment Variables](#environment-variables)
6. [Project Structure](#project-structure)

---

## <a name="overview">🧠 Overview</a>

**Banking Finance Management** is a production-grade financial platform that allows users to securely link multiple bank accounts via Plaid, view live transaction data, categorize spending, and transfer funds to other users through Dwolla — all from a single, responsive dashboard.

The project is built with a focus on security, performance, and clean architecture using server-side rendering with Next.js and TypeScript throughout.

---

## <a name="tech-stack">⚙️ Tech Stack</a>

| Layer | Technology |
|---|---|
| Framework | Next.js 14 (App Router) |
| Language | TypeScript |
| Auth & Database | Appwrite |
| Bank Linking | Plaid |
| Fund Transfers | Dwolla |
| Forms | React Hook Form + Zod |
| Styling | TailwindCSS + ShadCN UI |
| Charts | Chart.js |

---

## <a name="features">🔋 Features</a>

- **Secure Authentication** — Server-side auth with full validation and session management via Appwrite
- **Multi-Bank Linking** — Connect multiple bank accounts through the Plaid integration
- **Dashboard Overview** — Aggregated balance across all banks, recent transactions, and spending by category
- **Transaction History** — Paginated, filterable transaction list per bank account
- **Real-time Sync** — Account data updates automatically when new banks are connected
- **Fund Transfers** — Send funds to other platform users using Dwolla with full form validation
- **Fully Responsive** — Optimised for desktop, tablet, and mobile viewports

---

## <a name="getting-started">🚀 Getting Started</a>

### Prerequisites

Ensure you have the following installed:

- [Node.js](https://nodejs.org/en) (v18+)
- [npm](https://www.npmjs.com/)
- [Git](https://git-scm.com/)

### Clone the Repository

```bash
git clone https://github.com/anmolpra1/Banking-Finance-Management.git
cd Banking-Finance-Management
```

### Install Dependencies

```bash
npm install
```

### Configure Environment Variables

Create a `.env` file in the root directory and populate it with the values below (see [Environment Variables](#environment-variables) for details).

### Run the Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## <a name="environment-variables">🔐 Environment Variables</a>

Create a `.env` file at the root of your project:

```env
# NEXT
NEXT_PUBLIC_SITE_URL=

# APPWRITE
NEXT_PUBLIC_APPWRITE_ENDPOINT=https://cloud.appwrite.io/v1
NEXT_PUBLIC_APPWRITE_PROJECT=
APPWRITE_DATABASE_ID=
APPWRITE_USER_COLLECTION_ID=
APPWRITE_BANK_COLLECTION_ID=
APPWRITE_TRANSACTION_COLLECTION_ID=
APPWRITE_SECRET=

# PLAID
PLAID_CLIENT_ID=
PLAID_SECRET=
PLAID_ENV=sandbox
PLAID_PRODUCTS=auth,transactions,identity
PLAID_COUNTRY_CODES=US,CA

# DWOLLA
DWOLLA_KEY=
DWOLLA_SECRET=
DWOLLA_BASE_URL=https://api-sandbox.dwolla.com
DWOLLA_ENV=sandbox
```

You can obtain credentials by signing up at:
- [Appwrite](https://appwrite.io/)
- [Plaid](https://plaid.com/)
- [Dwolla](https://www.dwolla.com/)

---

## <a name="project-structure">🗂️ Project Structure</a>

```
├── app/                    # Next.js App Router pages
├── components/             # Reusable UI components
│   ├── bank/               # Bank-related components (BankInfo, BankDropdown, etc.)
│   └── ui/                 # ShadCN base components
├── lib/
│   ├── actions/            # Server actions (user, bank, dwolla, transactions)
│   ├── appwrite.config.ts  # Appwrite client setup
│   ├── plaid.config.ts     # Plaid client setup
│   └── utils.ts            # Utility functions
├── constants/              # App-wide constants
├── types/                  # TypeScript type definitions
└── public/                 # Static assets
```

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<div align="center">
  Built by <a href="https://github.com/anmolpra1">@anmolpra1</a>
</div>
