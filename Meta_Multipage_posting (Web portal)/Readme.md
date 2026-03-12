# Multipage Posting using Web Portal (Webhook): n8n Template

This workflow generates or processes multiple poster pages triggered by an incoming webhook request.

## Overview
A simple HTML webportal where input will given and that triggers webhook in n8n
The workflow receives input via webhook, splits the data into multiple items, processes them through APIs, and formats the final output.


## Nodes Used

- Webhook
- Split Out
- HTTP Request
- HTTP Request
- Edit Fields

## How It Works

1. The workflow starts when a **Webhook request** is received.
2. The input data is split into multiple items using **Split Out**.
3. Each item is processed through **HTTP Request nodes**.
4. **Edit Fields** prepares the final output.

## Setup

1. Import the workflow into **n8n**.
2. Copy the generated **Webhook URL**.
3. Configure the **HTTP Request nodes** with your APIs.
4. Send data to the webhook to trigger the workflow.

## Use Case

- API-driven poster generation
- Automation triggered from external apps
- Dynamic multi-page content processing
