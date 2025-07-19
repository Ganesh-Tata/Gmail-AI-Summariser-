AI-Powered Gmail Summarizer to Google Sheets
🚀 Project Overview
This project automates the process of summarizing your Gmail emails and neatly organizing those summaries into a Google Sheet. Leveraging the power of Google's Gemini API for intelligent text summarization and the robust infrastructure of Google Cloud Platform (GCP), this tool helps you quickly grasp the essence of your emails, saving time and boosting productivity.
✨ Features
 * Automated Email Fetching: Connects to your Gmail inbox to retrieve email content.
 * AI-Powered Summarization: Uses the Gemini API to generate concise summaries of email bodies.
 * Google Sheets Integration: Automatically populates a specified Google Sheet with email summaries and relevant metadata (e.g., sender, subject, date).
 * Secure Authentication: Utilizes GCP Service Accounts for secure and programmatic access.
 * Configurable: Easily adjustable for different Gmail labels or Google Sheet targets.
🛠️ Technologies Used
 * Gemini API (Generative Language API): For AI-driven text summarization.
 * Google Cloud Platform (GCP):
   * Gmail API: To interact with Gmail accounts.
   * Google Sheets API: To write data into Google Sheets.
   * Service Accounts: For secure authentication.
   * [Optional: Google Cloud Functions / Cloud Run / Cloud Scheduler if deployed serverlessly]
 * Python 3.x
 * Google API Python Client Library
⚙️ Setup & Installation
Follow these steps to get the project up and running:
1. Google Cloud Platform Setup
 * Create a GCP Project: If you don't have one, create a new project in the Google Cloud Console.
 * Enable APIs:
   * Go to APIs & Services > Enabled APIs & services.
   * Search for and enable the following APIs:
     * Gmail API
     * Google Sheets API
     * Generative Language API (for Gemini)
 * Create a Service Account:
   * Navigate to IAM & Admin > Service Accounts.
   * Click + CREATE SERVICE ACCOUNT.
   * Give it a name (e.g., gmail-summarizer-sa).
   * Grant the following roles (least privilege principle):
     * Gmail API User
     * Google Sheets Editor (or Viewer if you only plan to read from sheets)
     * Generative Language API User
 * Generate Service Account Key:
   * After creating the service account, click on the three dots under Actions for your new service account.
   * Select Manage keys > ADD KEY > Create new key > JSON.
   * A JSON file will be downloaded. Rename this file to credentials.json and place it in the root directory of your project. Keep this file secure! Do not share it publicly.
