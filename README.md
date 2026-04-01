🏥 Hospital Appointment System – n8n Workflow

📌 Overview

This project is a fully automated Hospital Appointment Booking System built using n8n.

It simulates real-world booking scenarios and handles:

✅ Appointment validation

⚠️ Missing data detection

🔁 Duplicate slot prevention

📩 Real-time notifications (Telegram + Gmail)

⚡ Key Highlights

✨ No-code + low-code automation

🧠 Smart validation logic

🔄 Duplicate detection using memory

📡 Webhook-based API system

📲 Multi-channel notifications



🔄 How It Works (Step-by-Step)

1️⃣ Webhook Trigger

API Endpoint:

POST /webhook/book-appointment

Starts the workflow

2️⃣ Load Test Users

Simulates 3 scenarios:

✅ Valid booking

⚠️ Missing field

🔁 Duplicate booking

3️⃣ Validation Node

Checks required fields:

Name
Doctor
Date
Time
Phone

👉 Missing fields → Error Flow

4️⃣ Error Flow

Sends alert via:

📲 Telegram

📧 Gmail

5️⃣ Slot Check Logic

Uses global workflow storage

Checks:

Doctor

Date

Time

6️⃣ Decision Outcomes
| Scenario       | Result    | Action |
| -------------- | --------- | ------ |
| ❌ Missing Data | Error     | Notify |
| 🔁 Duplicate   | Rejected  | Notify |
| ✅ Valid        | Confirmed | Notify |


📩 Notification System

📲 Telegram

Instant alerts
Booking confirmations
Duplicate warnings

📧 Gmail

Error reports
Appointment confirmations
Duplicate notifications

🧪 Sample API Request
{
  "name": "Rahul Sharma",
  "doctor": "Dr. Mehta",
  "date": "2026-04-05",
  "time": "10:00 AM",
  "phone": "9876543210"
}

📦 Project Structure

hospital-appointment-n8n/
│
├── README.md
├── workflow/
│   └── hospital-appointment-workflow.json
│
├── docs/
│   ├── architecture.md
│   └── screenshots/
│
├── examples/
│   └── sample-request.json
│
└── config/
    └── credentials-guide.md

⚙️ Setup Instructions

🔧 Step 1: Import Workflow

Open n8n
Click Import
Paste JSON file

🔐 Step 2: Configure Credentials

Telegram Bot API
Gmail OAuth2

▶️ Step 3: Activate Workflow

Enable workflow
Copy webhook URL

🧪 Step 4: Test API

curl -X POST http://localhost:5678/webhook/book-appointment

📌 Important Notes

⚠️ Data resets on each execution (demo purpose)
🧠 Uses in-memory storage (no database)
🔁 Designed for testing multiple scenarios



Kumar K

⭐ Show Your Support

<img width="2273" height="2243" alt="mermaid-diagram" src="https://github.com/user-attachments/assets/e82599b5-92a5-44cd-a857-9334beeb86a5" />

