# N8N_Workflows

This repository contains my personal [n8n](https://n8n.io) workflows created to automate various tasks such as sending emails, integrating APIs, managing files, and more. These are visual workflows built with n8n’s powerful drag-and-drop editor, designed to streamline repetitive processes and improve productivity.

---


---

## 🛠️ How to Use

1. Clone this repo:
   ```bash
   git clone https://github.com/your-user/N8N_Workflows.git
   cd N8N_Workflows


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

**📎 Sheet Reference Example:**
| Title       | Due Date  | Completion Date | Status     | Notes      | Deleted | ID        | Parent | Previous |
|-------------|-----------|------------------|------------|------------|---------|-----------|--------|----------|
| Example Task | 2025-08-01 |                  | needsAction | Example note | FALSE   | task12345 |        |          |

---

**📂 Node Flow:**


1. 🟢 Manual Trigger
   └─ Starts the workflow manually when testing or debugging.

2. 📗 Read Sheet (Google Sheets Node)
   └─ Reads rows from a specific sheet in Google Sheets.
   └─ Each row represents a task with fields like Title, Due Date, Notes, etc.

3. 🟠 Code Node
   └─ Transforms the data:
       - Converts text dates to ISO format.
       - Trims strings.
       - Handles optional fields like status, deleted, parent, and previous.
       - Prepares the correct structure for the Google Tasks API.

4. 🔵 Google Tasks Node
   └─ Creates a new task in your Google Task List based on the transformed data.




