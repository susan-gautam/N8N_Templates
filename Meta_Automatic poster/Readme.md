# Multipage Poster Generator – n8n Template

This workflow generates or processes multiple poster pages automatically using scheduled automation.

## Overview

The workflow triggers on a schedule, splits poster data into multiple items, processes each item through API requests, and formats the final output.

## Nodes Used

- Schedule Trigger
- Split Out
- HTTP Request
- HTTP Request
- Edit Fields

## How It Works

1. The **Schedule Trigger** starts the workflow automatically.
2. **Split Out** separates multiple poster items.
3. Each item is processed through **HTTP Request nodes**.
4. **Edit Fields** formats or prepares the final result.

## Setup

1. Import the template into **n8n**.
2. Configure the **HTTP Request nodes** with your API endpoints.
3. Adjust the **schedule trigger timing**.
4. Activate the workflow.

## Use Case

- Automated poster generation
- Bulk image or design processing
- Scheduled content generation
