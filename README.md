# JS TASKER PRO - Test Build, Phase 1 (Foundation)

Plain HTML, CSS and vanilla JS. No build step. Demo data is stored in this browser only (localStorage).

## Run
- Phone: unzip, upload the files to a GitHub repo, enable GitHub Pages, open the link.
- Computer: `python3 -m http.server`, then open http://localhost:8000
- Install: Chrome menu -> Install app (works over HTTPS or localhost).

## Files
index.html, manifest.json, sw.js, icons/, css/app.css, js/app.js

## Phase 1 contains
- The approved test build, re-branded to JS TASKER PRO. User IDs now look like JS-120986 (JS- + 6 digits).
- Split into index.html + css + js, installable PWA (manifest, offline shell, icons).
- Hidden admin: no admin button anywhere. On the login screen tap the logo 7 times quickly, then the Admin login box appears.
  - Admin ID: 01953866541
  - TEST password: Test@12345 (test build only; the final build uses Firebase Auth and you choose the password in the Firebase Console; it is never stored in code)
  - Admin auto-logs out after 30 minutes idle.
- Demo user: demo@jstasker.test / 1234
- All UI text is English.

## Decisions
- Test admin password lives in the demo data only because this build has no backend.
- The Bangla sample text from the reference screenshot is not used anywhere.
- Category marks (▶ ➤ ♪ ◎) are still text glyphs from the test build; Phase 3 replaces them with inline SVG icons.

## Next phases (one zip each)
2. Settings-driven app: every price, percent, limit and text editable in admin (money rules, levels, leaderboard, referral, categories with colors, methods with per-method bonus).
3. Screens matched to the reference screenshots (Create Task, Edit Task, Review, Wallet, History, Invite, Leaderboard, Profile, Live Chat, admin menu).
4. Final build: Firebase Auth + Firestore, security rules, money logic, deploy guide.
