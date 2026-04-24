# AI Email Automation: n8n Workflow

This n8n workflow automatically reads incoming Gmail messages, classifies them using Google Gemini AI, sends appropriate response emails, and updates email/contact status.

## Workflow Steps
1. Gmail Trigger fetches new emails every hour
2. Filters out internal emails (@syncbricks.com)
3. Checks if email is already a reply (avoids duplicates)
4. Extracts subject + body content
5. Gemini AI classifies the email into categories
6. Routes email based on classification:
   - Guest Post Inquiry
   - YouTube Video Inquiry
   - Course Inquiry
7. Sends predefined HTML response email
8. Marks email as read
9. Applies Gmail label
10. Saves/updates contact in Brevo

## AI Classification Logic
Input:
- Email Subject
- Email Body

Categories:
- Guest Post → blog collaboration / backlinks
- Youtube → video review / promotion requests
- Udemy Courses → training / course inquiries

## Setup Required
- Gmail OAuth2 credentials
- Google Gemini API key
- SMTP email credentials
- Brevo (Sendinblue) API key
- n8n instance (local or cloud)

## Output
Automated email handling with:
- Correct reply sent based on intent
- Email marked as read
- Label applied in Gmail
- Contact stored in Brevo

## Notes
- Ensure correct field usage:
  - `subject` (not `Subject`)
- Avoid running on internal emails
- Templates are static (can be upgraded to AI-generated replies)
