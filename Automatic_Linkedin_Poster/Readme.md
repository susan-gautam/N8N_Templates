# LinkedIn AI Post Generator – n8n Template

This n8n workflow automatically generates LinkedIn posts using AI and prepares them for publishing.

## Overview

The workflow runs on a schedule, sends a prompt to an AI API to generate content, formats the response, and prepares the final LinkedIn post content.

## Nodes Used

- Schedule Trigger
- HTTP Request (AI generation)
- Edit Fields
- HTTP Request (Post processing)

## How It Works

1. The workflow starts using a **Schedule Trigger**.
2. A request is sent to an **AI API** to generate LinkedIn post content.
3. The response is formatted using **Edit Fields**.
4. The final content is processed or sent to another API endpoint.

## Setup

1. Import the workflow into **n8n**.
2. Add your **AI API endpoint and key** in the HTTP Request nodes.
3. Adjust the **schedule trigger** if needed.
4. Activate the workflow.

## Use Case

- Automated LinkedIn content generation
- AI-powered social media posting
- Content automation workflows
