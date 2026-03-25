# AI Page Object Model (POM) Generator: n8n Workflow

## Overview

This n8n workflow automatically logs into a website, extracts HTML elements and generates a Page Object Model (POM) based on that html using AI, and saves the generated locators into Google Sheets.
Page Object Model (POM) a design pattern used in test automation to create an object repository for web UI elements, improving test maintenance, readability, and code reusability

The workflow is useful for QA automation engineers who want to automatically generate Selenium Page Object Models from a website.

## Workflow Process

The workflow performs the following steps:

1. Manual trigger starts the workflow.
2. Login credentials and target login URL are set.
3. The workflow logs into the website using a browser automation service.
4. HTML content is extracted from the logged-in page.
5. Interactive elements (buttons, inputs, forms, links, etc.) are extracted from HTML.
6. A prompt is generated and sent to an AI model.
7. The AI generates Page Object Model locators in JSON format.
8. The AI response is processed and formatted.
9. The locators are saved into Google Sheets.

## Nodes Used

* Manual Trigger
* Set (Login credentials and URL)
* HTTP Request (Browser Scraper API)
* Code (Extract HTML Elements)
* Code (Generate AI Prompt)
* HTTP Request (AI API / Gemini)
* Code (Extract AI Response)
* Google Sheets (Save POM Data)

## Google Sheets Output

The following fields are saved into Google Sheets:

* Element Name
* Locator Type
* Locator Value
* Description

## Setup Instructions

1. Import the workflow JSON into n8n.
2. Update login credentials and login URL in the **Set node**.
3. Configure the **Browser Scraper API / Browserless** endpoint.
4. Add your **AI API key** in the Gemini HTTP Request node.
5. Configure **Google Sheets credentials**.
6. Replace the Google Sheet ID and Sheet Name.
7. Execute the workflow.

## Use Case

This workflow can be used for:

* Selenium Page Object Model generation
* QA automation setup
* Test automation framework preparation
* Locator extraction from websites
* Automated UI element documentation

## Requirements

* n8n
* Browserless or Puppeteer API
* Google Sheets
* AI API (Gemini or similar)
* Website login credentials

## Notes

* The workflow extracts only interactive elements like buttons, inputs, forms, links, etc.
* AI must return the response in JSON format.
* The workflow stores generated locators in Google Sheets for further automation use.

---
