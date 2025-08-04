# N8N_Workflows

This repository contains my personal [n8n](https://n8n.io) workflows created to automate various tasks such as sending emails, integrating APIs, managing files, and more. These are visual workflows built with n8n’s powerful drag-and-drop editor, designed to streamline repetitive processes and improve productivity.

---

## 📁 Workflows Overview

| Workflow Name                          | Description                                    | Status   |
|---------------------------------------|------------------------------------------------|----------|
| Google Sheets → Google Tasks Sync     | Syncs tasks from a spreadsheet into Google Tasks | ✅ Done   |
| _More coming soon..._                 |                                                | 🚧 Planned |

---

## 🔧 Workflow Details

### 1️⃣ Google Sheets → Google Tasks Sync

**📄 File:** `google-sheets-to-tasks.json`

**🔗 Description:**
This workflow reads structured task data from a Google Sheet and syncs it into a Google Task list. It's useful for automating task imports or maintaining a shared task tracker in Sheets.

**🔍 Features:**
- Reads task data from Google Sheets
- Parses due/completion dates
- Optional fields: notes, deleted, parent/previous tasks
- Uses `Code` node for transformation logic
- Sends formatted tasks to Google Tasks API

**📌 Technologies Used:**
- Google Sheets API
- Google Tasks API
- JavaScript (inside Code node)

**▶️ Trigger:**
Manual Trigger (can be upgraded to cron or webhook)

**📂 Node Flow:**
