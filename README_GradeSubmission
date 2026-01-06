# CRS Grade Submission Extractor

A Google Colab–based automation tool for extracting, analyzing, and organizing **grade submission data** from the UP CRS system.  
The script scrapes class-level and student-level grade information, computes detailed statistics, and uploads structured outputs to a **shared Google Drive folder**, organized by academic term.

---

## ✨ Features

- Secure login to CRS (faculty credentials required)
- Interactive selection of **Academic Term**
- Automatic extraction of all assigned classes
- Auto-navigation to each **Assign Grades** page
- Student-level grade parsing and classification
- Detailed per-class analytics:
  - Total enrolled
  - No grade yet
  - Dropped
  - INC (uncompleted)
  - INC (completed → passing / failing)
  - 4.00 (unremoved)
  - 4.00 resolved → passing / failing
  - Passing and failing counts
  - Average grade (excluding INC-uncompleted, DRP, blank)
- Export of:
  - **Master summary sheet** (Excel)
  - **Per-class student grades** (JSON)
- Automatic upload to a **shared Google Drive folder**
- Automatic cleanup of local Colab files after upload

---

## 📁 Output Structure (Google Drive)
Main Drive Folder
└── 
├── master_summary_.xlsx
├── grades_<class_code_1>.json
├── grades_<class_code_2>.json
└── …

Each academic term has its own folder containing:
- One Excel summary file
- One JSON file per class (student-level data)

---

## 🛠 Requirements

### Environment
- Google Colab
- Internet access to CRS
- Google account with access to the shared Drive folder

### Python Libraries
Installed automatically in Colab:
- `selenium`
- `pandas`
- `pydrive2`
- `google-colab`
- Standard library: `json`, `re`, `collections`

---

## 🚀 Usage Guide

### 1. Open the Notebook in Google Colab

Upload or open:
Grade_Submission_Extractor.ipynb

---

### 2. Authenticate Google Drive

You will be prompted to log in to your Google account.

This allows the script to:
- Create folders
- Upload files
- Organize outputs per academic term

---

### 3. Provide CRS Credentials

Enter your CRS username and password when prompted.

> Credentials are used **only during the active Colab session** and are not stored.

---

### 4. Select Academic Term

The script detects all available academic terms and asks you to select one interactively.

---

### 5. Automated Extraction

For the selected term, the script:
- Scrapes all assigned classes
- Opens each “Assign Grades” page
- Parses and classifies student grades
- Computes per-class statistics
- Exports JSON and Excel outputs

---

### 6. Upload to Google Drive

All generated files are uploaded to the shared Drive folder under a subfolder named after the academic term.

---

### 7. Automatic Cleanup

After successful upload:
- All generated `.json` and `.xlsx` files are deleted from Colab
- Google Drive copies remain intact

---

## 📊 Grade Classification Rules

### Normal Grades

| Format | Classification |
|------|---------------|
| 1.00 – 3.00 | Passing |
| 4.00 | Conditional (unremoved) |
| 5.00 | Failing |

### INC Cases

| Format | Classification |
|------|---------------|
| INC | Uncompleted INC |
| INC (≤ 3.00) | Completed INC → Passing |
| INC (> 3.00) | Completed INC → Failing |

### 4.00 Resolution

| Format | Classification |
|------|---------------|
| 4.00 | Unremoved |
| 4.00 (≤ 3.00) | Removed → Passing |
| 4.00 (> 3.00) | Removed → Failing |

### Other

| Format | Classification |
|------|---------------|
| DRP / DROP / D | Dropped |
| Blank | No grade yet |

📌 **Average grade calculation excludes**:
- INC (uncompleted)
- Dropped students
- Blank / no grade entries

---

## 📄 JSON Output Format (Per Class)

Example: `grades_<class_name>.json`

```json
[
  {
    "student_no": "202312345",
    "name": "DELA CRUZ, JUAN",
    "program": "BS GE",
    "grade_raw": "INC (2.25)",
    "category": "inc_completed_pass",
    "numeric_grade": 2.25
  }
]

## 🔐 Data Privacy & Access Control
	•	Uploaded files inherit Google Drive sharing permissions
	•	Only users with access to the shared folder can view the outputs
	•	No CRS data is stored permanently in Google Colab

## ⚠️ Notes & Limitations
	•	Designed for manual or occasional execution in Google Colab
	•	Not intended for unattended scheduled jobs
	•	CRS UI changes may require selector updates
	•	Use responsibly and in compliance with institutional policies



