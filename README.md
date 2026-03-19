<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=ffc0cb&height=200&section=header&text=Cramberry&fontColor=ffffff&fontSize=40&animation=fadeIn"/>
</p>

<p align="center">
  <em>Study smarter, not harder. One cram at a time.</em> 🩷
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Made%20with-🩷%20love-ffc0cb?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Platform-PWA-ffb6c1?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Frontend-Vanilla%20JS-ffc0cb?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Hosted%20on-Netlify-ffb6c1?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Storage-GitHub-ffc0cb?style=for-the-badge"/>
</p>

---

## 🌸 What is Cramberry?

Cramberry is a pink-themed Progressive Web App (PWA) that turns your CSV reviewer files into interactive mock exams — straight from your phone, anytime, anywhere, even offline!

Cramberry is a personal study tool designed to make reviewing fun and accessible. Instead of scrolling through notes, you answer multiple-choice questions pulled directly from your own reviewer files stored on GitHub. It works like a real exam — with instant feedback, explanations, and a final score at the end.

No backend. No database. No subscriptions. Just you, your notes, and a little pink app. 🍓

---

## ✨ Features

- 🩷 Soft pink UI designed for comfort and focus
- 📂 Browse reviewers by subject — organized in folders
- 📋 Supports multiple subjects and multiple CSV files per subject
- 🔀 Shuffle questions for a fresh experience every session
- 🔢 Choose how many questions to answer per session
- ✅ Instant feedback after every answer
- 📖 Explanation shown right after each question
- 📊 Final score summary with pass/fail indicator
- 📲 Installable as a mobile app (Add to Home Screen)
- 📶 Works offline after first load (PWA)
- 🔁 Retry the same reviewer or go back to pick another

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript (Vanilla) |
| Hosting | Netlify (free) |
| File Storage | GitHub (public repository) |
| CSV Loading | GitHub Contents API + Raw GitHub URLs |
| Offline Support | Service Worker (PWA) |
| Fonts | Google Fonts — Playfair Display + Nunito |

---

## 📁 File Structure

```
cramberry/
├── index.html
├── manifest.json
├── service-worker.js
├── icon-192.png
├── icon-512.png
└── csv/
    ├── software-design/
    │   └── softdes_reviewer.csv
    ├── programming-paradigms/
    │   └── paradigms.csv
    ├── data-structures/
    │   └── data_structures.csv
    └── your-subject-here/
        └── your_reviewer.csv
```

The app reads everything inside the `csv/` folder automatically. Each subfolder is a subject, and each `.csv` file inside it is a reviewer.

---

## ⚙️ Setup Guide

### What You Need

- A free GitHub account
- A free Netlify account
- The Cramberry files (`index.html`, `manifest.json`, `service-worker.js`)

### Step 1 — Set Up Your GitHub Repository

1. Go to [github.com](https://github.com) and log in
2. Click **"+"** → **"New repository"**
3. Name it: `cramberry`
4. Set it to **Public** ✅
5. Click **"Create repository"**
6. Upload these files:
   - `index.html`
   - `manifest.json`
   - `service-worker.js`
   - `icon-192.png`
   - `icon-512.png`

### Step 2 — Add Your First CSV Reviewer

1. In your repo, click **"Add file"** → **"Create new file"**
2. In the filename box, type the full path like:
   `csv/software-design/softdes_reviewer.csv`
3. Paste your CSV content into the editor
4. Click **"Commit changes"**

> 💡 Typing a `/` in the filename automatically creates a folder in GitHub!

### Step 3 — Deploy to Netlify

1. Go to [netlify.com](https://netlify.com) and log in
2. Click **"Add new site"** → **"Import an existing project"**
3. Connect to GitHub and select your `cramberry` repo
4. Leave build settings blank
5. Click **"Deploy site"**

You'll get a free link like `https://cramberry.netlify.app` 🎉

> 💡 You can rename your site under **Site Settings → Change site name**

### Step 4 — Install on Your Phone 📲

**Android (Chrome):**
1. Open your Netlify link in Chrome
2. Tap ⋮ → **"Add to Home Screen"**
3. Tap **"Add"**

**iPhone (Safari):**
1. Open your Netlify link in Safari
2. Tap the Share button (□↑) at the bottom
3. Tap **"Add to Home Screen"**
4. Tap **"Add"**

Cramberry will appear as an app icon on your home screen! 🍓

---

## 📋 CSV Format

```
question, option_a, option_b, option_c, option_d, correct_answer, explanation
```

**Example Row:**

```
What is the heart's function?, Pump blood, Filter toxins, Digest food, Store energy, A, The heart is a muscular organ that pumps blood throughout the body delivering oxygen and nutrients to all tissues.
```

**Rules to Remember:**

- Column names must be exact and lowercase
- `correct_answer` must be `A`, `B`, `C`, or `D` (uppercase)
- If your explanation contains a comma, wrap the whole cell in double quotes
- Never leave `question` or `correct_answer` blank
- Do not add extra columns or rename existing ones

---

## ➕ How to Add New Reviewers

**Adding a new CSV to an existing subject:**

1. Go to your `cramberry` repo on GitHub
2. Click **"Add file"** → **"Create new file"**
3. Type the path: `csv/software-design/new_reviewer.csv`
4. Paste your CSV content
5. Click **"Commit changes"**

Netlify redeploys automatically in 1–2 minutes ✅

**Adding a brand new subject:**

1. Click **"Add file"** → **"Create new file"**
2. Type a new folder path: `csv/new-subject/reviewer.csv`
3. Paste your CSV content
4. Click **"Commit changes"**

The new subject will automatically appear in the app! 🩷

---

## 🔄 How the App Works

```
Open App
↓
Subjects load from GitHub (csv/ folder)
↓
Pick a Subject → Pick a Reviewer
↓
Set number of questions + shuffle
↓
Start Exam
↓
Answer questions
↓
See explanation
↓
Final Score
```

---

## 📶 Offline Mode

After your first visit, Cramberry caches its core files and works fully offline. However, loading new reviewers from GitHub requires an internet connection. Once a reviewer has been opened, it is not permanently cached.

---

## 🌱 Future Feature Ideas

- Bookmark mode
- Session history
- Dark mode
- Search
- Local CSV upload
- Streaks
- Tags
- Custom explanations

---

## ⚠️ Disclaimer

Cramberry is a personal study tool built for private, non-commercial use only. All reviewer content uploaded to this app is created and owned by the user. This project is not affiliated with any academic institution, publisher, or organization.

---

## 👩‍💻 About

Made with 🩷 and too much caffeine.

**Princess Mae V. Sanchez**
[github.com/cessamaeeee](https://github.com/cessamaeeee)

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=ffc0cb&height=120&section=footer"/>
</p>
