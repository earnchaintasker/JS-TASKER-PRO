# JS TASKER PRO - Full Test Build

Plain HTML, CSS and vanilla JS. No build step. Demo data lives in this browser only (localStorage).
This is the complete test version: every screen works with demo data so you can try the whole flow.

## Run
- Phone: unzip, push the files to a GitHub repo, enable GitHub Pages, open the link.
- Computer: `python3 -m http.server`, open http://localhost:8000
- Install: browser menu -> Install app.

## Files
index.html, manifest.json, sw.js, icons/, css/app.css, js/app.js

## Logins
- Demo user: demo@jstasker.test / 1234 (button on the login screen)
- Admin: no button anywhere. On the login screen tap the logo 7 times quickly. Admin ID 01953866541, TEST password Test@12345 (test build only). Auto logout after the idle minutes set in admin.

## What works
- Worker: tasks, filters, search, proof submit, history with tabs, levels with rewards, referral (link/code/stats), leaderboard (size from admin), profile edit, verify, live chat, notifications, dark mode.
- Buyer: create task (live total and afford line), my tasks, edit task, review proofs (approve, reject with reason), Top Job (charged only on confirm), delete request, expiry refund.
- Wallet: deposit (method bonus, fee, TrxID once, screenshot), withdraw (live BDT, fee, daily limit, password check, reject refunds).
- Admin: dashboard, deposits, withdraws, users, tasks, categories and prices (color, enable, price tools, percent change), payment methods (per-method bonus, fee, min, max, deposit/withdraw use), settings screen built from a schema (add one row in SCHEMA in js/app.js and a new option appears), audit log, backup/restore, purge.
- Everything numeric or textual comes from settings and changes live: money rules, fees, expiry, levels, referral, leaderboard, chat window, history days, app name, About, Terms, maintenance, registration on/off, ban message, auto-approve hours.

## Decisions
- The test admin password lives in demo data only because there is no backend. The real one is chosen in Firebase Console in the final build.
- Money is kept as dollars with 3 decimals here; the final build uses integer micro-dollars.
- Not in the test build (need a backend): real security, Firebase Auth, device limit, rate limits, email verification, push notifications, multi-level referral, disputes, tickets.

## Final build (next zip)
Firebase Auth + Firestore, security rules, money functions, seed script and deploy guide. It needs your Firebase project web config, so it is delivered separately.
