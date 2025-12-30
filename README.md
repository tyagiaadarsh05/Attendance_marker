

Project
A lightweight, client-side Attendance Management web app (single-file HTML) that stores data in the browser and supports Excel import/export.

Features
- Add / manage students and mark daily attendance
- Student view to check personal attendance records
- Export students to Excel and import from Excel/CSV (SheetJS)
- Automatic flexible column mapping during import (e.g., USN, Roll, ID, Name, Full Name)
- Local storage only — no backend required

Quick Start
1. Clone or download the repo.
2. Open `index.html` in your browser (or serve it: `python -m http.server 8000`).
3. Login as admin:
   - Default: username: admin | password: admin
4. Use the Admin panel to add students, mark attendance, or import/export student lists.

Import / Export details
- Export: click Export Students → downloads students.xlsx.
- Import: click Import Students and select `.xlsx`, `.xls`, or `.csv`.
  - The importer auto-detects columns (accepts variants like Roll, USN, StudentID, Name, Full Name).
  - Shows a preview of detected columns and sample rows before import.
  - Merges by USN — imported rows overwrite existing entries with the same USN.
- Sample file included: students.csv

Data storage & inspection
- Data is saved in browser localStorage under keys: admins, students, attendance
- To inspect: open DevTools → Application / Storage → Local Storage, or run in console:
  - JSON.parse(localStorage.getItem('students'))

Notes & Customization
- Styling/background in `style.css` — edit to change image, opacity, or layout.
- SheetJS is loaded via CDN; no build step required.

Contributing & License
Contributions welcome — open an issue or PR. Add a license of your choice.
