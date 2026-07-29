# Job Application Tracker

A command-line Python program that helps a user record job applications, saves
them to a Word document, and emails the report to the user via the Gmail API.
Built as a Continuous Assessment project for the Diploma in Python Programming
(CCT College Dublin).

---

## What it does

The user manages job applications through a simple menu.  The program can:

1. Collect job applications from the user (company, role, status, date applied).
2. Save all applications to a `.docx` report, named with the current date in
   `year-month-day` format (e.g. `job_applications_2026-07-28.docx`).
3. Log in through the Gmail API (OAuth 2.0) and email the report to the user as
   an attachment.
4. Move the report into a `logs/` folder once it has been sent.

## Additional features

-  **Persistent storage (JSON):** applications are saved to `applications.json`
  and reloaded automatically when the program starts, so data is not lost
  between runs.
-  **Statistics:** the program can display the total number of applications and a
  breakdown by status (Applied, Interviewing, Offer, Rejected).


---

## Requirements

- Python
- Google account (Gmail and Drive APIs)
- Python packages:
  - `python-docx`
  - `google-api-python-client`
  - `google-auth-httplib2`
  - `google-auth-oauthlib`