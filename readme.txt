# Project README

## Overview

This repository contains an HTML-based Receipt Generator tool that connects directly to a Google Sheets document. The system automates the recording of receipt data, making it easy for users to generate receipts and instantly store them in the linked spreadsheet.

## How It Works

* The **HTML interface** serves as the front-end of the tool where users fill out receipt fields.
* When the user clicks **"Fill Receipts"**, the data is automatically sent to the connected Google Sheet using Google Apps Script.
* All logic for transmitting data is handled using a **Google Apps Script** stored within the same Google Sheets document.

## Linked Google Sheet

Receipt submissions are automatically added here:
**Google Sheet:** [https://docs.google.com/spreadsheets/d/1zd0gMCKXyFzaOGRcCtQAlCtjRi3ayLiN7UhbmGhDAU0/edit?gid=0#gid=0](https://docs.google.com/spreadsheets/d/1zd0gMCKXyFzaOGRcCtQAlCtjRi3ayLiN7UhbmGhDAU0/edit?gid=0#gid=0)

This sheet also contains the script that processes incoming data.

## Website / Launcher

A simple index page is included that links to the Receipt Generator HTML and the Google Sheet. When hosted (or opened locally), users can click **Open Receipt Generator** to launch the application.

* **Index (website) file:** `index.html` — links to `Pag-Ibing Naga-Alimbukad.html` and the Google Sheet.

## Google Apps Script

The Google Apps Script extension inside the sheet:

* Receives data from the HTML form
* Appends the data into the appropriate rows
* Handles validation and automation logic

The script must remain published as a **Web App** so the HTML file can communicate with it.

## Files in This Repository

* **index.html** – The UI where users input receipt details
* **script.js** *(if applicable)* – Handles front-end submission logic
* **README.md** – Documentation for set‑up and usage

## Requirements

* A Google account
* Permissions to edit the linked Google Sheet
* Google Apps Script deployed as a Web App with "Anyone with the link" access

## Deployment Instructions

To deploy and fully connect the Receipt Generator to Google Sheets, follow these steps:

### 1. Deploy the Google Apps Script as a Web App

1. Open the linked Google Sheet.
2. Go to **Extensions → Apps Script**.
3. In the Apps Script editor, click **Deploy → New Deployment**.
4. For **Type**, choose **Web App**.
5. Set:

   * **Execute as:** *Me (your Google account)*
   * **Who has access:** *Anyone with the link*
6. Click **Deploy**.
7. Copy the **Web App URL** and paste it into the Receipt Generator (HTML) where it asks for the script URL.

### 2. Connect the HTML to the Script

* Open `Pag-Ibing Naga-Alimbukad.html` in your browser.
* Paste the Web App URL into the configuration field.
* The HTML will now send data to your Google Sheet.

### 3. Host / Use the Website

You can choose any of these options:

* **Local:** Double-click `index.html` and use it offline.
* **GitHub Pages:** Upload the repository to GitHub → Settings → Pages → Select Branch → Save.
* **Google Drive Hosting:** Upload the HTML files and use third-party static hosting (if needed).

### 4. Updating the Script

Whenever you edit the Google Apps Script:

* Go to **Deploy → Manage Deployments**
* Click the deployment → **Edit** → **Deploy** again
* Update the HTML if the Web App URL changes

---

## Usage

1. Open the HTML file in any browser.
2. Enter all required receipt details.
3. Press **Fill Receipts**.
4. Check the Google Sheet to confirm the data has been added.

## Notes

* Editing the Google Apps Script may break the connection if the Web App is not redeployed.
* Make sure CORS and permissions are correctly configured in the script.

## Contact

For issues or updates, ensure that the Google Sheet and script access are properly configured for all collaborators.
