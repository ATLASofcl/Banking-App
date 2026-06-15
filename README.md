# 🏦 Banking App

A simple, menu-driven **command-line banking application** written in pure Python. Create an account, log in securely, and manage your money: deposits, withdrawals, transfers, and a full transaction history, all from your terminal.

Built as a university course project to put core Python skills into practice: classes, file I/O, JSON persistence, input validation, and a clean interactive CLI.

> ℹ️ This is an educational project, not a real banking system. See the [security note](#-security-note) below.

---

## ✨ Features

- 🔐 **Accounts & login**: sign up and log in with hidden password entry (no on-screen echo)
- 🔢 **PIN-protected actions**: a 4-digit PIN confirms every deposit, withdrawal, and transfer
- 💸 **Core banking**: check balance, deposit, withdraw, and transfer between accounts
- ⭐ **Top payees**: frequently used transfer recipients are surfaced for quick selection
- 🧾 **Transaction history**: every action is timestamped and listed per account
- ✅ **Input validation**: positive amounts only, 4-digit numeric PINs, and no empty or numeric usernames
- ↩️ **Easy navigation**: type `b` or `back` at most prompts to step back
- 💾 **Automatic persistence**: data is saved to `accounts.json` and the file is created on first run

---

## 📦 Requirements

- **Python 3.10 or newer** (the code uses modern type-hint syntax such as `str | None`)
- **No third-party dependencies**: everything runs on the Python standard library

---

## 🚀 Getting Started

Clone the repository and run the app:

```bash
git clone <repository-url>
cd Banking-App
python main.py
```

That's it. No installation or setup required. Exit the app at any time with `Ctrl+C`.

---

## 🧭 Usage

When you launch the app you'll see the main menu:

```
=== Banking App ===
Main Menu (Ctrl+C to exit app)

1) Login
2) Sign Up
```

After logging in, you land in your account dashboard:

```
=== Banking App - joe_doe ===
Logged in (Ctrl+C to exit app)

1) Check Balance
2) Deposit
3) Withdraw
4) Transfer
5) View Transaction History
6) Logout
```

Deposits, withdrawals, and transfers each ask for your **4-digit PIN** before going through. Transfers let you pick from your top payees or enter a recipient's username directly.

---

## 🗂️ Project Structure

```
Banking-App/
├── main.py         # The entire application: menus, account logic, and persistence
└── accounts.json   # Account data store (auto-created on first run if missing)
```

All account data is stored as JSON: each user record holds a password, PIN, balance, and a list of timestamped transactions.

---

## 🔒 Security Note

This project is for **learning purposes only**. Passwords and PINs are stored in plain text in `accounts.json`, and there is no encryption, hashing, or real authentication. **Do not use it with real financial information.**

---

## 👥 Authors

Contributors:
- [@ATLASofcl](https://github.com/ATLASofcl)
- [@Arshia532](https://github.com/Arshia532)
