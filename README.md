# hackathon-finder
# ⚡ HackMatch — Hackathon Team Finder

A web app for college students to find teammates for hackathons, built for **State College of Engineering** (easily rebranded).

---

## 📌 What is HackMatch?

HackMatch helps students form teams for hackathons. Instead of scrambling to find a UI designer or ML engineer at the last minute, students can create a profile showcasing their skills and browse others who are looking to team up.

---

## ✨ Features

### 👤 Profile Creation
- Register with your name, college email, year, and department
- Set your primary role (e.g. Frontend Developer, ML Engineer, UI/UX Designer)
- Write a bio describing what you bring to a team
- Select your skills from 50+ tech tags (React, Python, Figma, Docker, etc.)
- Add your GitHub / Portfolio link
- Toggle your availability status — let others know if you're open to team up

### 🔍 Browse & Find People
- See all registered students as profile cards
- Search by name, skill, or role
- Filter by role category (Backend, UI/UX, Data Analyst, etc.)
- Filter by availability (Open to Teams / Not Available)
- Click any card to view a full profile

### ✉️ Team Requests
- Send a personalised team request to any available student
- Include your hackathon name and a message explaining your project
- Recipient receives the request in their inbox (Requests tab)
- Accept or decline incoming requests

### 🔔 Notifications
- Red dot indicator on the Requests tab when new requests arrive

---

## 🗂️ Project Structure

```
hackathon-finder.html   ← The entire app (single HTML file)
README.md               ← This file
```

The entire app is a **single self-contained HTML file** — no build tools, no server, no dependencies required.

---

## 🚀 How to Run

1. Download `hackathon-finder.html`
2. Open it in any modern browser (Chrome, Firefox, Edge, Safari)
3. That's it — no installation needed!

---

## 🛠️ How to Customise

### Change the College Name
Open `hackathon-finder.html` in a text editor and find:

```
STATE COLLEGE OF ENGINEERING
```

Replace it with your actual college name. It appears in the nav badge.

### Add or Remove Skills
Find the `SKILL_LIST` array in the `<script>` section and add/remove skill strings:

```javascript
const SKILL_LIST = [
  'React', 'Vue', 'Python', ...
];
```

### Add or Remove Role Options
Search for `<option>Frontend Developer</option>` and edit the `<select>` dropdowns for role options in both the register form and the browse filter.

### Change Seed / Demo Profiles
Find the `users` array in the script and edit or remove the pre-loaded student objects. Each user has this shape:

```javascript
{
  id: 1,
  name: 'Aditya Menon',
  email: 'aditya@college.edu',
  year: '3rd Year',
  dept: 'Computer Science',
  role: 'Full Stack Developer',
  bio: 'Love building end-to-end web apps...',
  skills: ['React', 'Node.js', 'MongoDB'],
  github: 'https://github.com/handle',
  available: true,
  requests: []
}
```

---

## 🔐 Authentication Note

The current version uses **in-memory storage** (data resets on page refresh). It is designed as a prototype / demo. To make it production-ready for your college, you would integrate:

- A backend (Node.js / Django / Firebase)
- A real database (MongoDB / PostgreSQL / Firestore)
- College SSO or email-based authentication

---

## 🧱 Tech Stack

| Layer | Technology |
|---|---|
| UI | HTML5, CSS3 (CSS Variables), Vanilla JavaScript |
| Fonts | Sora (Google Fonts), JetBrains Mono |
| Icons | Unicode emoji (no external icon library) |
| Storage | In-memory JavaScript arrays (prototype) |
| Dependencies | None — fully self-contained |

---

## 📋 Roles Supported

- Frontend Developer
- Backend Developer
- Full Stack Developer
- UI/UX Designer
- ML / AI Engineer
- Data Analyst
- DevOps Engineer
- Mobile Developer
- Cybersecurity
- Business / PM

---

## 🗓️ Roadmap (Suggested Future Features)

- [ ] Persistent storage with a backend / Firebase
- [ ] College email verification (OTP)
- [ ] In-app messaging / chat
- [ ] Hackathon listings page (upcoming events)
- [ ] Team builder — create a team and post an open invite
- [ ] Profile endorsements / ratings after hackathons
- [ ] Admin dashboard for college coordinators

---

## 👥 Contributing

This project was built for internal college use. To suggest improvements or report issues, contact the developer or raise it with your college tech club.

---

## 📄 License

Built for **State College of Engineering** — for internal student use only.
