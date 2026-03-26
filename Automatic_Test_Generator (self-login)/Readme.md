# AI Test Case Generator – n8n Workflow

This n8n workflow logs into a web dashboard, extracts HTML content, sends it to Google Gemini AI to generate functional test cases, and saves the test cases into Google Sheets.

## Workflow Steps
1. Manual Trigger starts the workflow
2. Login credentials are set
3. Browserless logs into the dashboard
4. HTML content is extracted
5. Gemini AI generates test cases
6. Test cases are parsed
7. Data is saved to Google Sheets

## Setup Required
- Browserless Docker container
- Google Gemini API Key
- Google Sheets OAuth connection
- Login credentials for target website

## Output
Generated test cases with:
- Test Case ID
- Test Scenario
- Test Steps
- Expected Result
- Priority
- Result