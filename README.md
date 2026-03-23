# Telegram Expense Tracker with OCR (n8n Workflow)

## Overview
This n8n workflow allows you to track expenses and income directly from Telegram using both text messages and receipt images. It uses AI to extract structured data and stores it in Google Sheets.

## Features
- 📩 Process text messages from Telegram
- 🧾 Extract data from receipt images (OCR)
- 🤖 AI-powered expense and income parsing
- 📊 Automatically save data to Google Sheets
- ✅ Send confirmation messages back to Telegram

## How It Works

### Text Flow
1. User sends a message (e.g. "Spent 10 on lunch")
2. AI extracts:
   - Type (Expense/Income)
   - Amount
   - Category
   - Description
   - Date

### Image Flow
1. User sends a receipt image
2. OCR extracts text from the image
3. AI processes the extracted text into structured data

### Final Step
- Both flows are merged
- Data is formatted
- Saved to Google Sheets
- Confirmation message is sent to the user

## Requirements
- n8n
- Telegram Bot API credentials
- Groq API key
- Mistral API (for OCR)
- Google Sheets account

## Setup
1. Import the workflow into n8n
2. Connect all required credentials:
   - Telegram
   - Groq
   - Mistral
   - Google Sheets
3. Update the Google Sheets document ID
4. Activate the workflow

## Example Inputs

**Text:**Spent 25 on dinner


**Image:**
- Upload a receipt photo in Telegram

## Output (Google Sheets)
- Date
- Type
- Amount
- Description

## Notes
- Works with both text and image inputs
- AI ensures structured and clean data
- Make sure your Telegram bot is active

---
Simple automated expense tracking 🚀
