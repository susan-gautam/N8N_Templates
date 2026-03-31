# Locator Testing Automation: n8n Workflow

## Overview

This n8n workflow automatically logs into a web dashboard, reads locators from Google Sheets (user have to provide), verifies whether the locators exist in the HTML, and writes PASS/FAIL results back to another Google Sheet.
This is Hybrid model QA Automation method. If google sheets has 100s of locater value then, it can verify about locaters.
Example locaters: href="/dashboard"
NOTE: this works only for in house made websites and cannot bypass security of Top level websites like Amazon, Meta and others

## Workflow Steps

1. Manual trigger starts workflow
2. Login credentials are set
3. Browserless logs into dashboard
4. Locators are read from Google Sheet
5. HTML is checked for locator presence
6. PASS/FAIL result generated
7. Results saved to Testing_Results sheet

## Google Sheets Required

Sheet 1: **POM**

* Element Name
* Locator Value

Sheet 2: **Testing_Results**

* Timestamp
* Locator
* Status
* Note

## Requirements

* n8n
* Browserless (Docker)
* Google Sheets OAuth
* Dashboard login credentials

## Output

The workflow generates:

* PASS if locator found
* FAIL if locator missing
* SKIPPED if locator empty
* Login Error if login fails
