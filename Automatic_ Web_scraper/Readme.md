# Web Scraper to Google Sheets: n8n Workflow

This n8n workflow scrapes quotes, authors, and tags from a website and automatically appends or updates the data in a Google Sheet.

## Overview

The workflow performs the following steps:

1. Triggered manually using **Execute Workflow**.
2. Sends a request to the website to fetch quote data.
3. Extracts quotes, authors, and tags using an HTML parsing node.
4. Processes the extracted data using a JavaScript node.
5. Appends or updates the data into a specified Google Sheet.

## Nodes Used

- Manual Trigger
- HTTP Request
- HTML Extract
- JavaScript (for data formatting)
- Google Sheets (Append or Update Row)

## Setup

1. Import the workflow JSON into **n8n**.
2. Configure the **Google Sheets node** with your spreadsheet ID and sheet name.
3. Run the workflow manually or schedule it if needed.

## Use Case

- Automated scraping of quotes and authors
- Storing structured data in Google Sheets for analytics or dashboards
- Quick data collection for personal or educational projects
