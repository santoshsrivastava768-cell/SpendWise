# SpendWise — Smart Insights + Authentication Prototype

## Run locally

1. Install Node.js (LTS) if it is not installed.
2. Open this folder in VS Code. It must contain `package.json`.
3. In the terminal, run `npm install` (on Windows PowerShell, `npm.cmd install` also works).
4. Run `npm run dev` (or `npm.cmd run dev`).
5. Open the local URL printed by Vite, usually http://localhost:5173/.

## Authentication included

- Sign up with a name, email, and password (minimum 8 characters).
- Sign in and sign out.
- Passwords are hashed with the browser Web Crypto SHA-256 API before local storage.
- SpendWise transactions, accounts, pending items, and budget are stored under a per-email browser-local key so separate demo users have separate local data.

## Important security limitation

This is a **frontend authentication prototype**, not production authentication. User records and hashes remain in localStorage and can be inspected or altered by someone with access to the browser. Client-side hashing is not a substitute for server-side password hashing, secure sessions, HTTPS, rate limiting, or access controls. Do not use a real or reused password. For production, add a backend API (for example Node.js/Express), a database, server-side password hashing such as Argon2id/bcrypt, and secure HttpOnly cookies.

The project uses fictional demo transactions and does not connect to real bank accounts.
