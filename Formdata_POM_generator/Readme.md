# AI Page Object Model Generator: n8n Workflow

## Overview

This n8n workflow logs into a web application, extracts HTML elements, uses Google Gemini AI to generate Page Object Model (POM) locators, and saves the locators into Google Sheets.

## Workflow Steps

1. Manual trigger starts workflow
2. Login credentials are set
3. Browserless logs into the website
4. HTML interactive elements are extracted
5. Gemini AI generates POM locators
6. JSON response is parsed
7. Locators saved to Google Sheets

## Google Sheet Columns

* Element Name
* Locator Type
* Locator Value
* Type (Form Data / Metadata)

## Requirements

* n8n
* Browserless (Docker)
* Google Gemini API Key
* Google Sheets OAuth
* Website login credentials

## Output

Automatically generated Page Object Model (POM) locators ready for Selenium automation.
