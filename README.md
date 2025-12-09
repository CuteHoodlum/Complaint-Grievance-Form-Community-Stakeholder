# Complaint-Grievance-Form-Community-Stakeholder
📌 Overview

This project is a fully responsive HTML5 form designed for recording community or stakeholder complaints / grievances.
It includes a clear sectioned layout, auto-filled dates, print/PDF support, integrated signature upload, and a light/dark mode toggle.
The form is ideal for field teams, HSE officers, customer service units, and project-based grievance management systems.

✨ Features
✔ Modern UI / UX

Clean card-based layout

Responsive grid system

Works on desktops, tablets, and mobile devices

✔ Dark / Light Mode

A toggle button switches between themes (body.dark-mode styles).

✔ Structured Sections

Basic Information

Complainant Details

Category of Complaint

Description

Immediate Actions

Escalation & Investigation

Resolution / Action Plan

Closure & Signature

✔ Signature Upload

Accepts image files (PNG, JPG, etc.)

Shows preview

Includes “Remove Image” button

✔ Auto-Date Population

On page load, key date fields are automatically filled with today’s date.

✔ Print / Save as PDF

A built-in button triggers browser printing for PDF export.
Print stylesheet removes unnecessary UI elements and ensures clean formatting.

📂 File Structure
project-folder/
│
├── index.html              # Main form
├── Prado logo.png          # Logo displayed at top
├── android-chrome-512x512.png   # Favicon
└── README.md               # Documentation (this file)

🧠 How It Works
Dark Mode Toggle

Triggered by clicking the button:

document.getElementById("modeToggle").addEventListener("click", () => {
  document.body.classList.toggle("dark-mode");
});

Auto-fill Today’s Date

Executed when the page finishes loading:

document.addEventListener("DOMContentLoaded", () => {
  const today = new Date().toISOString().slice(0, 10);
  const dateIds = [
    "cg_date_received",
    "cg_incident_started",
    "cg_date_escalated",
    "cg_target_date",
    "cg_actual_closed"
  ];
  dateIds.forEach((id) => {
    const el = document.getElementById(id);
    if (el && !el.value) el.value = today;
  });
});

Signature Upload Preview

Controlled through <input type="file"> and an associated preview container.

🖨️ Print & PDF Export

The Print / Save as PDF button uses:

<button onclick="window.print()">🖨️ Print / Save as PDF</button>


Custom @media print CSS removes:

Buttons

Placeholders

Shadows and decorative styles

🚀 Usage Instructions

Open index.html in any modern browser.

Fill out all required fields.

Upload signature image (optional).

Click Print / Save as PDF to export a completed complainant record.

Save the PDF according to your organization’s filing system.

🛠 Customization
You can easily customize:

Logo (Prado logo.png)

Section names and fields

Styling (colors, border radius, spacing)

Additional validations

Export-to-JSON or backend integration

If you want, I can generate:
✅ A version with field validation
✅ A version with localStorage auto-save
✅ A React / Vue component
✅ A backend API (Node/PHP/Firebase)

📝 License

This form can be used freely within your organization for data collection and documentation.
