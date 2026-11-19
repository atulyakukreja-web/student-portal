# Student Portal — Academic Management System

A responsive, modern College Student Portal built with **HTML5**, **CSS3** (Custom Properties, CSS Grid, Flexbox), and **Vanilla JavaScript**. Inspired by modern university portals (CUIMS / AMS).

## Features

- **Authentication & Registration (`index.html`)**:
  - Sign In & Register tabs, Role selector (`Student` / `Faculty` / `Admin`)
  - UID/Password validation, password visibility toggle, Forgot Password modal
  - Quick demo auto-fill & session persistence via `sessionStorage`
- **Dashboard (`dashboard.html`)**:
  - Collapsible sidebar navigation + sticky top bar with global search, notification dropdown, and profile menu
  - 4 Overview Metric Cards: Overall Attendance (with SVG progress ring), Current SGPA/CGPA, Enrolled Courses, Pending Fee Balance
  - Live Widgets: Today's Class Schedule (highlights active slot), Recent Notices feed (urgent items flagged), Upcoming Deadlines tracker
- **Attendance Tracker (`attendance.html`)**:
  - Overall attendance ring + subject-wise breakdown table
  - Threshold color-coding: Safe (≥ 85% Green), Caution (75–84% Amber), Shortage Warning (< 75% Red)
- **Courses & Syllabus (`courses.html`)**:
  - Active subject cards with syllabus progress bars
  - Lecture notes download action + interactive Assignment Submission modal (updates deadlines live)
- **Examinations & Results (`results.html`)**:
  - Semester tab switcher (Semester 4 & Semester 5)
  - Mid-Term, End-Term, Practical marks table with automatic grade calculation & GPA cards
- **Fee Payment Ledger (`fees.html`)**:
  - Fee structure breakdown + outstanding dues alert
  - Payment history table with downloadable fee receipts (`.txt`)
- **Academic Calendar (`calendar.html`)**:
  - Interactive monthly calendar with event markers + full Mon–Fri weekly timetable
- **Notices & Events (`notices.html`)**:
  - Category filter + debounced keyword search + expandable notice cards
- **My Profile (`profile.html`)**:
  - Personal, Contact, and Academic details + Edit Profile modal (persists during session)

## Demo Credentials

| Role | UID / ID | Password |
|---|---|---|
| **Student** | `22BCS10045` | `student123` |
| **Faculty** | `FAC2024` | `faculty123` |
| **Admin** | `ADM2024` | `admin123` |

## Project Structure

```text
student-portal/
├── index.html              # Login & Registration page
├── dashboard.html          # Main Dashboard
├── attendance.html         # Subject-wise Attendance Tracker
├── courses.html            # Courses, Syllabus & Assignment Submission
├── results.html            # Semester Marks & GPA Sheet
├── fees.html               # Fee Structure, Ledger & Receipts
├── calendar.html           # Academic Calendar & Weekly Timetable
├── notices.html            # Searchable Notices & Events
├── profile.html            # Student Profile & Edit Modal
├── css/
│   ├── variables.css       # Design tokens (colors, fonts, spacing)
│   ├── base.css            # Reset, typography & utility classes
│   ├── layout.css          # Shared header, sidebar & responsive shell
│   ├── components.css      # Cards, tables, badges, modals, toasts
│   └── pages.css           # Login & dashboard-specific styles
├── js/
│   ├── data/mockData.js    # Centralized mock student & academic data
│   ├── auth.js             # Simulated login, registration & auth guard
│   ├── layout.js           # Sidebar toggle, dropdowns & notifications
│   ├── modal.js            # Reusable modal open/close handler
│   ├── toast.js            # Toast notification system
│   ├── search.js           # Header global search across pages, courses & notices
│   ├── dashboard.js        # Dashboard widgets & metrics
│   ├── attendance.js       # Attendance calculations & threshold logic
│   ├── courses.js          # Course cards & assignment submission
│   ├── results.js          # Semester switching & grade calculation
│   ├── fees.js             # Fee summary & receipt download
│   ├── calendar.js         # Month calendar & weekly schedule
│   ├── notices.js          # Category & keyword filtering
│   └── profile.js          # Profile rendering & edit persistence
└── assets/
    ├── logo.svg
    └── avatar-placeholder.svg
```

## How to Run Locally

1. **Direct Open**: Double-click `index.html` to open in Chrome, Edge, or Firefox.
2. **Local Server (Recommended for full multi-page session consistency)**:
   - Using VS Code **Live Server**: Right-click `index.html` → *Open with Live Server*.
   - Or using Python:
     ```bash
     cd student-portal
     python -m http.server 8000
     ```
     Then open `http://localhost:8000` in your browser.
