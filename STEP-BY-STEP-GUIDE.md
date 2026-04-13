# 🏠 Family Budget App — Step-by-Step Deployment Guide

## What You'll Get
A family budget app with a shareable link that works like a native app on any phone.
All family members see the same data in real time.

---

## STEP 1: Set Up Firebase (Free Database) — 5 minutes

Firebase gives you a free real-time database so all family members stay in sync.

1. Go to **https://firebase.google.com**
2. Click **"Go to Console"** (top right)
3. Sign in with your Google account
4. Click **"Create a project"**
5. Name it `family-budget` → Click Continue
6. Turn OFF Google Analytics (not needed) → Click Create Project
7. Wait for it to finish → Click Continue

### Enable the Database:
8. In the left sidebar, click **"Build" → "Firestore Database"**
9. Click **"Create database"**
10. Choose **"Start in test mode"** → Click Next
11. Pick a location close to you (e.g., `europe-west1` for Israel) → Click Enable

### Get Your Firebase Config:
12. Click the **⚙️ gear icon** (top left) → **"Project settings"**
13. Scroll down → Click the **</>** (Web) icon to add a web app
14. Name it `family-budget` → Click **"Register app"**
15. You'll see a code block with `firebaseConfig = { ... }`
16. **Copy these values** — you'll need them in Step 3:
    - apiKey
    - authDomain
    - projectId
    - storageBucket
    - messagingSenderId
    - appId

---

## STEP 2: Set Up Vercel (Free Hosting) — 3 minutes

1. Go to **https://vercel.com**
2. Click **"Sign Up"** → Sign up with your **GitHub** account
   - If you don't have GitHub: go to **https://github.com** and create a free account first
3. Once signed in, you're ready for Step 3

---

## STEP 3: Upload the Project to GitHub — 5 minutes

1. Go to **https://github.com/new**
2. Name the repository: `family-budget`
3. Keep it **Public** → Click **"Create repository"**
4. Click **"uploading an existing file"** link
5. **Drag and drop ALL the project files** (the entire contents of the folder I gave you)
6. Click **"Commit changes"**

### Add your Firebase config:
7. In GitHub, open the file `src/firebase.js`
8. Click the **pencil icon** ✏️ to edit
9. Replace the placeholder values with YOUR Firebase config from Step 1
10. Click **"Commit changes"**

---

## STEP 4: Deploy on Vercel — 2 minutes

1. Go to **https://vercel.com/new**
2. Find your `family-budget` repository → Click **"Import"**
3. Framework Preset: select **"Vite"**
4. Click **"Deploy"**
5. Wait 1-2 minutes... ✅ Done!
6. You'll get a link like: **https://family-budget-xxxxx.vercel.app**

---

## STEP 5: Install on Your Phone — 1 minute

1. Open the Vercel link on your **Android phone** in Chrome
2. Tap the **⋮ menu** (three dots, top right)
3. Tap **"Add to Home screen"**
4. Tap **"Add"**
5. The app icon now appears on your home screen! 🎉

### Share with family:
6. Send the same link to your family members via WhatsApp/SMS
7. They do the same: open in Chrome → Add to Home Screen
8. Everyone is now connected to the same budget! 💰

---

## 🎉 You're Done!

Your family budget app is now live. Everyone can:
- Add expenses and see them appear instantly for all members
- Track spending by category
- See who spent what
- Use it like a native app from the home screen

---

## Troubleshooting

**App shows blank page?**
→ Make sure you updated `src/firebase.js` with your real Firebase config

**Data not syncing?**
→ Check that Firestore is in "test mode" (Step 1, point 10)

**Can't find "Add to Home Screen"?**
→ Make sure you're using Chrome browser on Android

**Need to change the currency?**
→ Edit `src/App.jsx`, find `CURRENCY = "₪"` and change it
