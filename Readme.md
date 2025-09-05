# HireMate Automation Workflow

## Overview

This workflow automates the end-to-end process of handling job applications received via Gmail, extracting resume data, screening candidates, scheduling HR interviews, and updating Google Sheets for tracking. It leverages AI for resume parsing and candidate communication, Google Drive for storing resumes, and Google Calendar for interview scheduling.

## Features

- **Email Trigger:** Monitors Gmail for new job applications and inquiries.
- **Resume Extraction:** Downloads resume attachments and extracts text from PDF files.
- **AI Resume Parsing:** Uses AI to extract candidate details (name, email, phone, skills, education, experience, etc.) from resumes and checks if the candidate matches the MERN stack developer job description.
- **Google Drive Integration:** Uploads resumes to a designated folder in Google Drive.
- **Candidate Screening:** Automatically shortlists candidates who match the job criteria and sends personalized replies.
- **Interview Scheduling:** Parses candidate availability from email replies, checks Google Calendar for free slots, and schedules HR interviews with Google Meet links.
- **Google Sheets Integration:** Updates two sheets:
  - **Resume Spreadsheet:** Stores parsed candidate details and match status.
  - **Interview Schedules:** Logs scheduled interviews with date, time, and meeting URL.
- **Automated Communication:** Sends confirmation and follow-up emails to candidates.

## Workflow Steps

1. **Trigger:** The workflow starts when a new email is received.
2. **Switch:** Routes emails based on subject (e.g., "Apply", "Re").
3. **Resume Handling:** For applications, downloads and extracts resume data.
4. **AI Parsing:** Uses OpenAI to parse resume and check job match.
5. **Google Drive:** Uploads resume files.
6. **Google Sheets:** Appends or updates candidate info.
7. **Shortlisting:** If matched, sends a shortlist email and requests interview availability.
8. **Availability Parsing:** Uses AI to extract availability from candidate replies.
9. **Calendar Scheduling:** Books interview slots and generates Google Meet links.
10. **Confirmation:** Sends interview details and updates the interview schedule sheet.

## Technologies Used

- **n8n** workflow automation
- **Gmail API** for email handling
- **Google Drive API** for file storage
- **Google Sheets API** for data tracking
- **Google Calendar API** for interview scheduling
- **OpenAI GPT-4** for AI parsing and communication

## Setup Instructions

1. **Credentials:** Ensure Gmail, Google Drive, Google Sheets, Google Calendar, and OpenAI API credentials are configured in n8n.
2. **Google Drive Folder:** Update the folder ID for resume storage if needed.
3. **Google Sheets:** Set the correct document and sheet IDs for candidate and interview tracking.
4. **Calendar:** Use the correct calendar email for scheduling.
5. **Activate Workflow:** Enable the workflow in n8n for automation.

## Customization

- **Job Description:** Modify the AI prompt in the workflow to change the job criteria.
- **Interview Time Window:** Adjust the time window in the AI prompt and calendar nodes as needed.
- **Sheets Schema:** Update Google Sheets columns to match your organization's requirements.

## License

This workflow is provided as-is for internal use. Please ensure compliance with your organization's data privacy policies.

---

**Contact:** For support or customization,