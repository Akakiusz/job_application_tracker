# Job Application Tracker

A command-line Python program that helps a user record job applications, saves
them to a Word document, and uploads the report to Google (Drive + Gmail).
Built as a Continuous Assessment project for the Diploma in Python Programming
(CCT College Dublin).

> **Status:** Work in progress. This README will be updated as features are completed.

---

## What it does

The user enters details of the jobs they have applied for (company, role,
status, date, notes). The program then:

1. Collects the application data from the user.
2. Saves a report as a `.docx` file, named with the download date.
3. Uses a web API to log in and upload the data:
   - **Google Drive API** – uploads the `.docx` report to the user's Drive.
   - **Gmail API** – emails the user a copy / confirmation.
4. Once the upload succeeds, the file is moved into a `logs/` folder.

## Additional features
 
- Filter applications by status (e.g. show only "interview").
- Simple statistics (how many applications, how many in each status).
- Input validation (allowed status values, required fields).

---

## Requirements

- Python
- Google account (Gmail and Drive APIs)
- Python packages:
  - `python-docx`
  - `google-api-python-client`
  - `google-auth-httplib2`
  - `google-auth-oauthlib`