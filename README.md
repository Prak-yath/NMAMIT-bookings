# 📅 NMAMIT Campus Bookings — 2026 Edition

A fast, mobile-first web app for booking halls, labs and grounds at **NMAMIT** using one shared calendar. Students request a venue, the admin approves it, and everyone can see what is free at a glance.

🔗 **[Live Demo](https://claude.ai/artifact/KLp4bqNJMZhTYUYyMWQQS6)**

---

## 📑 Table of Contents

- [About the Project](#-about-the-project)
- [Features](#-features)
  - [Core Booking](#core-booking)
- [Booking Workflow](#-booking-workflow)
- [Controls](#-controls)
- [Accessibility & Usability](#-accessibility--usability)
  - [Accessibility Options](#accessibility-options)
  - [Layout Modes](#layout-modes)
- [Visual & UI Design](#-visual--ui-design)
- [Data & Storage](#-data--storage)
- [Responsive Design](#-responsive-design)
- [Technical Stack](#-technical-stack)
  - [No External Dependencies](#no-external-dependencies)
- [Original vs. 2026 Edition](#-original-vs-2026-edition)
- [Getting Started](#-getting-started)
  - [Option 1 — Open the Live Page](#option-1--open-the-live-page)
  - [Option 2 — Run Locally](#option-2--run-locally)
- [Project Structure](#-project-structure)
- [Current Status](#-current-status)
- [Future Improvements](#-future-improvements)
- [Inspiration](#-inspiration)
- [Team](#-team)
- [License](#-license)
- [References](#-references)

---

## 🎓 About the Project

Booking campus venues usually means chasing people, checking spreadsheets and finding out about clashes too late. **NMAMIT Campus Bookings** replaces that with a single page where:

- anyone with an `@nmamit.in` or `@nitte.in` email can see the **common calendar**,
- a date tap shows **which venues are free** and for which hours,
- an **admin** approves or rejects each request.

**Venues covered:** Sambhram, Shambhavi, Amphi theatre, Abhyuday Hall, Sadananda, Phalguni, BC Alva Ground, ISLO2 (lab), ISLO3 (lab), ISLO4 (lab).

---

## ✨ Features

### Core Booking

- 📆 **Shared month calendar** with coloured dots for every booked venue
- 🟢 **Free-venue list** for any selected date, with an hour-by-hour availability bar per venue
- ⚠️ **Clash detection** — overlapping bookings at the same venue are blocked
- ✅ **Approval workflow** — requests start as *Pending*, then become *Approved* or *Rejected*
- ✏️ **Edit and cancel** your own bookings (an edit goes back for approval)
- 🔁 **Recurring bookings** — repeat weekly for up to 12 weeks
- 📝 **Booking details** — title, club or department, attendees, contact number, notes and equipment
- 📋 **My Bookings** view with live status
- 📥 **Add to calendar** — download an approved booking as an `.ics` file (Google, Outlook, Apple)
- 🛡️ **Admin panel** — pending approvals, date blocking (exams, maintenance) and usage chart
- 🔍 **Venue filter** chips to focus the calendar on one place

---

## 🔄 Booking Workflow

| Step | Who | What happens |
|------|-----|--------------|
| 1. Check | Student | Tap a date and see free venues and time bars |
| 2. Request | Student | Fill the form and submit; status is **Pending** |
| 3. Review | Admin | Approves or rejects from the Admin panel |
| 4. Confirmed | Student | Booking shows **Approved** and can be added to a calendar |

**Rules built in**

- Bookings run **8 AM – 8 PM**, up to **8 hours** each
- Pending requests hold their slot, so nobody can double-book while waiting
- Admins can block dates for one venue or all venues
- Admins are exempt from the time-of-day and duration limits

---

## 🎯 Controls

| Action | Desktop | Mobile |
|--------|---------|--------|
| Pick a date | Click a day | Tap a day |
| Change month | `‹` `›` buttons | Swipe the calendar left or right |
| Switch panel | Availability / Schedule / Book tabs | Bottom tab bar |
| Choose a venue to book | Click it in the Availability list | Tap it |
| Filter by venue | Click a chip | Scroll the chips and tap |
| Left/right-hand layout | — | **L / R** switch in the header |
| Sign out | **Sign out** button | **Sign out** button |

---

## ♿ Accessibility & Usability

### Accessibility Options

- Large touch targets and 16 px form text on phones
- Dark mode follows the device setting automatically
- Respects **reduced motion** — animations switch off when the device asks for it
- Clear status labels, never colour alone (text badges: Free, Partly booked, Blocked, Pending)

### Layout Modes

- 🤚 **Right-handed** — tab bar order puts *Book* under the right thumb
- 🤚 **Left-handed** — tab bar order reverses and action buttons move to the left
- The choice is remembered on the device

---

## 🎨 Visual & UI Design

- Soft gradient background with frosted-glass cards
- Maroon accent colour with matching dark theme
- Smooth animations: fade-up cards, sliding month changes, popping dots, a sliding tab highlight and confirmation toasts
- Floating, thumb-friendly bottom navigation on phones

---

## 💾 Data & Storage

- Bookings, approval decisions and blocked dates live in the page's shared database, so everyone sees the same calendar
- Your email (student) and handedness choice are remembered on your device
- An admin login lasts until the browser tab is closed
- Sign out clears the saved email and the admin session

---

## 📱 Responsive Design

- Two-column layout on desktop: calendar left, details right
- Single column on phones with a fixed bottom tab bar
- Works on any modern browser; an internet connection is required to share bookings

---

## 🛠️ Technical Stack

| Layer | Choice |
|-------|--------|
| Markup, style, logic | Plain **HTML, CSS and JavaScript** in a single file |
| Shared data | Page database with three collections: `bookings`, `decisions`, `blocks` |
| Identity | Email gate for students, password gate for admin |
| Hosting | Published as a hosted page |

### No External Dependencies

No frameworks, no build step, no libraries to install. Everything is in one `nmamit-bookings.html` file.

---

## 🔄 Original vs. 2026 Edition

| | Original | 2026 Edition |
|---|---|---|
| Calendar | Basic month grid | Animated grid, swipe, venue filter |
| Availability | Booked list only | Free / partly booked / blocked per venue with hourly bars |
| Booking | Instant | Request → approval workflow |
| Roles | Everyone equal | Student and Admin |
| Booking options | Single slot | Edit, cancel, weekly repeats, details |
| Mobile | Shrunk desktop | Bottom navigation, swipe, left/right-hand layout |
| Export | None | Add to calendar (`.ics`) |

---

## 🚀 Getting Started

### Option 1 — Open the Live Page

1. Open the **[Live Demo](https://claude.ai/artifact/KLp4bqNJMZhTYUYyMWQQS6)**.
2. Choose **Student** and enter your `@nmamit.in` or `@nitte.in` email, or choose **Admin** and enter the admin password.
3. Tap a date, pick a venue and book.

### Option 2 — Run Locally

1. Download `nmamit-bookings.html`.
2. Open it in a browser.
3. Without the hosted database the page runs in **preview mode**: bookings stay on your device and are not shared.

---

## 📂 Project Structure

```
.
├── nmamit-bookings.html   # the whole app (markup, styles, logic)
└── README.md              # this file
```

---

## 🧪 Current Status

**Working**

- Shared calendar, free-venue list and hourly availability bars
- Student and Admin sign-in, approvals, date blocking and usage chart
- Edit, cancel, recurring bookings and calendar download
- Mobile layout with left/right-hand modes, dark mode and animations

**Known limitations**

- The email check for students is a simple gate, not verified single sign-on
- The admin password is checked inside the page, so it is a soft lock rather than strong security
- Clash checks run in the browser, so two simultaneous requests for the same slot could both go through; the admin can reject the duplicate
- No email notifications — students check **My Bookings** for status

---

## 🔮 Future Improvements

- 🔐 Real college login (single sign-on) and server-side permissions
- 📧 Email and push notifications for approvals and reminders
- 🏛️ Venue capacity, equipment lists and department-wise approval routing
- 📊 Exportable reports and utilisation analytics
- 🔎 Search and "find the next free slot" suggestions
- 📴 Installable app with offline viewing

---

## 💡 Inspiration

Ideas were drawn from established booking tools such as **25Live** (campus event and room scheduling with approvals), **Skedda** (visual booking with rules), **Robin** and **Clearooms** (live availability views).

---

## 👥 Team

| Name | Role |
|------|------|
| _Your name_ | _Project lead_ |
| _Teammate_ | _Role_ |

---

## 📄 License

Add your preferred license here (for example MIT) before publishing the repository.

---

## 📚 References

[1] J. D. German, D. C. G. Yap, and G. O. Binoya, “Design and Development of an Integrated Room Reservation System for Higher Education Institutions,” in *Proc. 2021 IEEE 8th Int. Conf. Ind. Eng. Appl. (ICIEA)*, 2021, doi: [10.1109/ICIEA52957.2021.9436766](https://doi.org/10.1109/ICIEA52957.2021.9436766).

[2] J. R. V. Jeny, P. Sadhana, B. J. Kumar, S. L. Abhishek, and T. S. Chander, “A Web based-College Event Management System and Notification Sender,” in *Proc. 2022 4th Int. Conf. Inventive Res. Comput. Appl. (ICIRCA)*, 2022, pp. 1434–1438, doi: [10.1109/ICIRCA54612.2022.9985774](https://doi.org/10.1109/ICIRCA54612.2022.9985774).

[3] M. Murin, F. Jakab, and M. Michalko, “Advanced reservation system,” in *Proc. 2021 19th Int. Conf. Emerging eLearning Technol. Appl. (ICETA)*, Košice, Slovakia, 2021, pp. 267–275, doi: [10.1109/ICETA54173.2021.9726673](https://doi.org/10.1109/ICETA54173.2021.9726673).

[4] S. Atkinson and K. Lee, “Design and Implementation of a Study Room Reservation System: Lessons from a Pilot Program Using Google Calendar,” *College & Research Libraries*, vol. 79, no. 7, pp. 916–930, Nov. 2018, doi: [10.5860/crl.79.7.916](https://doi.org/10.5860/crl.79.7.916).
