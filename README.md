# Municipal Street Light Fault Register & Repair Tracker

A simple web application to help municipal offices register, track, and manage street light fault complaints efficiently.

This project was developed using only **HTML, CSS, JavaScript, and Local Storage** without any backend or database.

---

# Problem Statement

Municipal street light complaints are often recorded manually, making it difficult to track repairs, identify repeated failures, and monitor pending complaints.

This application digitizes the complaint register, allowing operators to record, update, search, filter, and monitor street light faults in a simple dashboard.

---

# Features

- View all street light fault reports
- Add new complaint
- Edit existing complaint
- Delete complaint
- Instant Search
- Filter by Status
- Filter by Ward
- Dashboard Statistics
- Automatically calculate Days Pending
- Data saved using Local Storage
- Dark Mode
- Export records as CSV
- Responsive Design
- Loading, Empty and Error States
- Data persists after page refresh

---

# Technologies Used

- HTML5
- CSS3
- Vanilla JavaScript (ES6)
- Browser Local Storage

No backend or external libraries were used.

---

# Project Structure

```
Street-Light-Tracker/
│
├── index.html
```

---

# Dataset Fields

| Field | Description |
|--------|-------------|
| fault_id | Unique complaint ID |
| pole_id | Street light pole number |
| ward | Municipal ward |
| street | Street name |
| reported_date | Date complaint was reported |
| fault_type | Type of street light fault |
| status | Pending / In Progress / Repaired |
| repaired_date | Date complaint was repaired |

---

# Sample Fault Types

- Bulb Failure
- Pole Damage
- Wiring Issue
- Light Flickering
- Complete Outage
- Sensor Failure
- Electrical Fault
- Timer Issue
- Physical Damage
- Dim Light

---

# Status Values

- Pending
- In Progress
- Repaired

---

# Derived Value

## Days Pending

The application automatically calculates the number of days for every complaint.

### Formula

If Status = Repaired

```
Days Pending = Repaired Date − Reported Date
```

Otherwise

```
Days Pending = Today's Date − Reported Date
```

This value updates automatically whenever a complaint is edited.

---

# Dashboard

The dashboard displays

- Total Complaints
- Pending Complaints
- Repaired Complaints
- Longest Pending Complaint

These statistics update automatically after every operation.

---

# Search & Filter

Users can search by

- Fault ID
- Pole ID
- Ward
- Street Name
- Fault Type

Filters available

- Status
- Ward

---

# Data Storage

This project uses **Browser Local Storage**.

All records remain saved even after refreshing or reopening the website.

No database or server is required.

---

# How to Run

1. Download or Clone the repository

```
git clone https://github.com/yourusername/street-light-tracker.git
```

2. Open the project folder.

3. Double-click **index.html**

OR

Open it using **Live Server** in VS Code.

That's it.

No installation required.

No backend required.

---

# Testing

The application has been tested for:

- Add Complaint
- Edit Complaint
- Delete Complaint
- Search
- Filter
- CSV Export
- Dark Mode
- Pagination
- Local Storage Persistence
- Loading State
- Empty State
- Validation Errors

---

# Validation Rules

- Pole ID cannot be empty.
- Ward cannot be empty.
- Street cannot be empty.
- Reported Date cannot be a future date.
- Status is mandatory.
- Repaired Date is required when Status is "Repaired".
- Repaired Date cannot be earlier than Reported Date.

---

# Screenshots

<img width="1917" height="901" alt="image" src="https://github.com/user-attachments/assets/599179ad-2f54-4d89-aea9-1a4c77d63153" />
<img width="1917" height="913" alt="Screenshot 2026-07-26 204841" src="https://github.com/user-attachments/assets/9eecdc90-ddb5-4f2e-8386-eebc0e44024e" />
[Screen Recording 2026-07-26 204425 - Trim (2).zip](https://github.com/user-attachments/files/30389673/Screen.Recording.2026-07-26.204425.-.Trim.2.zip)


# Future Improvements

- Login Authentication
- Admin Dashboard
- Email Notifications
- GPS Location Mapping
- Complaint Images
- Real Database Integration
- Google Maps Support
- SMS Alerts
- Multi-user Access
- Cloud Deployment

---

# Known Limitations

- Uses Local Storage instead of a database.
- Works only in the current browser.
- No user authentication.
- No real-time synchronization.
- No map integration.

---

# Author

**Jaisarathi V**

B.Tech Artificial Intelligence and Data Science

GitHub: https://github.com/jaisarathi5

LinkedIn: https://www.linkedin.com/in/jai-sarathi-v-546a38385/

---

# 📄 License

This project is developed for educational purposes as part of the **SIH 2026 Practical Assessment**.
