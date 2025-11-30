Linked Google Sheet

Receipt submissions are automatically added here: Google Sheet: https://docs.google.com/spreadsheets/d/1zd0gMCKXyFzaOGRcCtQAlCtjRi3ayLiN7UhbmGhDAU0/edit?gid=0#gid=0

This sheet also contains the script that processes incoming data.

Google Apps Script

The Google Apps Script extension inside the sheet:

Receives data from the HTML form

Appends the data into the appropriate rows

Handles validation and automation logic

The script must remain published as a Web App so the HTML file can communicate with it.

Files in This Repository

index.html – The UI where users input receipt details

script.js (if applicable) – Handles front-end submission logic

README.md – Documentation for set‑up and usage

Requirements

A Google account

Permissions to edit the linked Google Sheet

Google Apps Script deployed as a Web App with "Anyone with the link" access

Usage

Open the HTML file in any browser.

Enter all required receipt details.

Press Fill Receipts.

Check the Google Sheet to confirm the data has been added.