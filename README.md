# In & Out Laundry  
**XISD6329/w – Work Integrated Learning 3B**  
**Team: Code Wave Solutions**

| Member | Student Number | Role |
|--------|----------------|------|
| Phelo Gusha | ST10314655 | UI/UX & QA Specialist |
| Ludumo Mathetha | ST10449894 | Lead Developer |
| Chulumanco Iviwe Ngongomana | ST10457499 | Frontend & Mobile Developer |

---

## Project Overview

In & Out Laundry is a digital laundry management solution consisting of:

- A **responsive website** for customers to view services, register/login, book collections, track orders and manage settings.
- An **Android mobile application** (Kotlin) that mirrors the core customer journey.
- A **shared backend / API + relational database**.
- **Admin capabilities** to view all bookings and update order status.

This repository contains the **website prototype** (ready to open in a browser) plus supporting documentation for the full Task 2 submission.

---

## Website Prototype (Current)

### How to run
1. Download / clone the repository.
2. Open `index.html` in any modern browser (Chrome, Edge, Firefox).
3. No server required for the prototype – it uses **LocalStorage** as a temporary data store.

> **Important for final marks:** Replace LocalStorage with a real API + database (Firebase, Node/Express + PostgreSQL/MySQL, or similar). The prototype clearly demonstrates the flows that must be backed by persistent storage.

### Demo Accounts
| Role     | Email                          | Password    |
|----------|--------------------------------|-------------|
| Customer | thabo@example.com              | Customer1!  |
| Admin    | admin@inandoutlaundry.co.za    | Admin123!   |

### Pages
- `index.html` – Home / marketing
- `services.html` – Service catalogue & prices
- `booking.html` – Create a new booking
- `login.html` / `register.html` – Authentication
- `dashboard.html` – Customer order history
- `settings.html` – Update profile & password
- `admin.html` – Admin view of all bookings + status updates

### Features implemented in prototype
- Registration & Login (password stored as base64 for demo only – **must be properly hashed / use Firebase Auth in final version**)
- Create booking with validation
- View personal order history
- Update account settings
- Admin status management
- Responsive UI that handles invalid input gracefully

---

## Database Schema

See `docs/database_schema.sql`.

Core tables:
- `users`
- `services`
- `bookings`
- `payments` (optional)
- `booking_status_history` (optional)

**Requirement:** Populate each main table with **at least 10 records**.

---

## Recommended Final Architecture (Task 2)

| Layer | Technology Suggestion |
|-------|-----------------------|
| Mobile App | Kotlin + Android Studio (Material Design 3) |
| Authentication + SSO | **Firebase Authentication** (Email/Password + Google Sign-In) |
| Database | Firebase Firestore **or** PostgreSQL / MySQL via REST API |
| API | Firebase Cloud Functions **or** Node.js / Express |
| Website | HTML/CSS/JS connected to the same API (or migrate to a simple React/Vue front-end) |
| CI/CD | GitHub Actions (build + unit tests) |
| Project Management | Azure DevOps Kanban board |
| Source Control | This GitHub repository – frequent commits |

### Must-have features for the Android app (from module manual)
- [ ] Register & Login with **encrypted passwords**
- [ ] Single Sign-On (SSO) – Google Sign-In via Firebase is the easiest route
- [ ] Settings screen (update name, phone, password, notification preferences)
- [ ] View services & create booking
- [ ] Track order status
- [ ] User-friendly UI that does not crash on invalid input
- [ ] Automated unit / instrumentation tests run via **GitHub Actions**
- [ ] App runs on a **real Android device** (required for the demonstration video)

---

## GitHub & DevOps

- Create / use the repository: `https://github.com/LudumoMathetha/In-and-Out-Laundry` (or the team’s official repo).
- Regular commits from every team member.
- GitHub Actions workflow for Android build + tests (see marketplace action linked in the module manual).
- Keep Azure DevOps Kanban board updated throughout the sprint.

---

## Demonstration Video Checklist

Record on a **physical Android phone** (not only emulator):
1. Registration / Login (including SSO if implemented)
2. Creating a booking
3. Viewing order status
4. Changing settings
5. Admin status update (if applicable)
6. Show data in the online authentication service, API and database
7. Professional voice-over explaining each step

Upload as unlisted YouTube video and place the link in this README.

---

## Release Notes (Template – update for final version)

### v1.0.0 – Prototype (Task 1 / early Task 2)
- Responsive website with full customer journey
- LocalStorage-backed authentication and bookings
- Admin dashboard for status management
- Database schema designed

### v1.1.0 – Full Implementation (update when ready)
- Android app with Kotlin
- Firebase Auth + SSO
- Real database + API
- Automated tests via GitHub Actions
- [List any innovative features here]

---

## Folder Structure

```
in-and-out-laundry/
├── index.html
├── services.html
├── booking.html
├── login.html
├── register.html
├── dashboard.html
├── settings.html
├── admin.html
├── css/
│   └── styles.css
├── js/
│   └── app.js
├── docs/
│   └── database_schema.sql
├── images/          (add screenshots / wireframes)
└── README.md
```

---

## Next Steps for the Team

1. **Ludumo** – Set up Firebase project (Auth + Firestore or Cloud SQL) and start Android project in Android Studio.
2. **Chulumanco** – Implement mobile screens (Login, Home, Booking, Orders, Settings) and connect to API.
3. **Phelo** – Write unit tests, prepare user documentation / help content, update Azure DevOps board, assist with UI polish and video planning.
4. Replace all LocalStorage calls with real API calls.
5. Record the demonstration video on a real device.
6. Keep committing regularly and update this README with release notes and the video link.

---

**Module:** XISD6329/w – Work Integrated Learning 3B  
**Institution:** The Independent Institute of Education  
**Year:** 2026
