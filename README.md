Municipal Street Light Fault Register & Repair Tracker
A full‑featured single‑page web application for managing street light complaints, with simulated server‑side validation and search.


📖 Table of Contents
Overview

Key Features

Technology Stack

Installation & Setup

How to Use

Server‑Side Validation

Server‑Side Search

Project Structure

Screenshots

Contributing

License

🚀 Overview
This application helps municipal authorities register, track, and manage street light fault reports. It provides a clean dashboard, full CRUD operations, bulk actions, dark mode, and data export – all in a single HTML file.

The project demonstrates two key server‑side behaviours (simulated in the browser for demonstration):

Server‑side validation – The Pole ID field is validated against a set of rules (format, uniqueness) by a simulated server, with clear error messages.

Server‑side search – The search box queries a simulated server endpoint that returns only the matching records, instead of filtering locally.

These changes make the application more realistic and prepare it for integration with a real backend.

✨ Key Features
📊 Dashboard & Chart – See total, pending, repaired, and longest‑pending complaints at a glance, plus a status distribution chart.

🔍 Server‑Side Search – Search by Pole ID, Ward, Street, Fault Type, or Fault ID. The server returns only matching records.

✏️ Full CRUD Operations – Add, edit, and delete complaints with a modal form that includes real‑time validation.

✅ Bulk Actions – Select multiple records to update their status in bulk or delete them all at once.

📥 Export Data – Download your data as CSV or JSON.

🌙 Dark Mode – Toggle between light and dark themes (preference saved in localStorage).

⌨️ Keyboard Shortcuts – Ctrl+N to add a new record, Ctrl+F to focus the search, Esc to close modals.

📱 Responsive – Works on desktops, tablets, and mobile devices.

💾 Local Storage – All data is persisted in your browser.

🛠️ Technology Stack
HTML5 – Semantic markup

CSS3 – Custom properties (theming), Flexbox, Grid, animations

JavaScript (ES6) – Vanilla JS, async/await, Promises, DOM manipulation

LocalStorage – Client‑side data persistence

No external libraries or frameworks are used – everything is vanilla for maximum portability.

📦 Installation & Setup
This is a single‑page application, so no build tools or server are required.

Clone the repository:

bash
git clone https://github.com/yourusername/street-light-fault-tracker.git
cd street-light-fault-tracker
Open the index.html file in your browser:

Double‑click the file, or

Use a local development server (e.g., VS Code Live Server, Python http.server, etc.)

That’s it! The application will load with sample data automatically.

🧑‍💻 How to Use
🔹 Server‑Side Validation (Pole ID)
When adding or editing a complaint, the Pole ID field is validated by a simulated server.
The validation checks:

Not empty – A message appears if the field is blank.

Format – Must be in the format P-XXXX where X is a digit (3 or 4 digits after the dash).
✅ Examples: P-1024, P-2056
❌ Examples: P-123, P-12A, 1024, P-12345

Uniqueness – The ID cannot already exist in the system (case‑insensitive).

As you type, a spinner appears while the “server” checks the value.
If the ID is invalid, a clear error message is shown next to the field, and the form will not submit until the error is fixed.

🔹 Server‑Side Search
The search box at the top sends your query to a simulated server, which returns only the matching records.
The search works across:

Pole ID

Ward

Street

Fault Type

Fault ID

Matching records – The result count updates (e.g., ✨ 3 matches), and the table shows only those records.

No matches – The table shows an empty state with a message like “No complaints found for ‘your‑term’” – not an error.

Clear the search – Leave the search box empty to see all records again.

A loading indicator appears while the server is processing your request.

Other Features
Dashboard – All metrics and the chart update automatically based on the current filtered data.

Bulk Actions – Select checkboxes, then use the bulk bar to update status or delete multiple records at once.

Export – Click the CSV or JSON buttons to download the current (filtered) data.

Dark Mode – Click the moon/sun icon in the header to toggle themes.

📁 Project Structure
text
street-light-fault-tracker/
├── index.html          # Single file containing all HTML, CSS, and JavaScript
└── README.md           # This file
The entire application is self‑contained in one HTML file for simplicity. In a real project, you would split the CSS and JS into separate files.

Fork the repository.

Create a new branch (git checkout -b feature/your-feature).

Commit your changes (git commit -m 'Add some feature').

Push to the branch (git push origin feature/your-feature).

Open a pull request.

📄 License
This project is licensed under the MIT License – see the LICENSE file for details.

🙏 Acknowledgements
Icons and emojis used for better UX.

Inspired by real‑world municipal fault management systems.

Happy tracking! 💡🔧
