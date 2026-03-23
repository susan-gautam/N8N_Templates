# AI Test Case Generator from Website – n8n Workflow

## Overview

This n8n workflow automatically generates functional test cases for any website using AI and saves the generated test cases into Google Sheets.
The workflow fetches website content, extracts readable text, sends it to an AI API to generate test cases, and stores the results in a Google Sheet.

## Workflow Process

The workflow follows these steps:

1. Manual trigger starts the workflow.
2. Target website URL is set.
3. Website content is fetched using a browser/content service.
4. HTML content is cleaned and converted into readable text.
5. A prompt is generated for the AI model.
6. AI generates functional test cases in JSON format.
7. The AI response is processed and formatted.
8. Test cases are saved to Google Sheets.

## Nodes Used

* Manual Trigger
* Set
* HTTP Request (Fetch Website Content)
* Code (Extract Page Text)
* Code (Generate Prompt)
* HTTP Request (AI API Request)
* Code (Process AI Response)
* Google Sheets (Save Data)

## Google Sheets Output

The following fields are saved into Google Sheets:

* Test Case ID
* Test Scenario
* Test Steps
* Expected Result
* Priority

## Setup Instructions

1. Import the workflow JSON into n8n.
2. Set the target website URL in the **Set Target URL** node.
3. Configure the **AI API Request** node with your AI service.
4. Add your **Google Sheets credentials**.
5. Replace the Google Sheet ID in the Google Sheets node.
6. Execute the workflow.

## Use Case

This workflow can be used for:

* Automated test case generation
* QA automation
* Website testing documentation
* AI-assisted software testing
* Test management automation

## Notes

* The workflow extracts only the first portion of website content to send to AI.
* AI must return test cases in JSON format.
* Google Sheets is used to store and manage generated test cases.

