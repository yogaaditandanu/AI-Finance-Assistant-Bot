# 🤖 AI Finance Assistant Bot

![Banner Image](link_ke_gambar_workflow_kamu_disini.png)

A smart Telegram bot that automates personal finance tracking using **n8n**, **Google Gemini AI**, and **Google Sheets**. This agent can read receipts from photos, understand natural language chats, and generate automated financial reports.

## 🚀 Features

-   **Receipt OCR:** Upload a photo of a shopping receipt, and the AI extracts the Merchant, Date, Items, and Total Amount automatically.
-   **Natural Language Processing:** Just type *"Bought coffee for 20k"* and it logs the transaction correctly.
-   **Automated Reporting:** Ask *"Show me this week's report"* and get a summarized breakdown via chat.
-   **Data Persistence:** All data is safely stored in Google Sheets for further analysis.

## 🛠️ Tech Stack

-   **Orchestrator:** [n8n](https://n8n.io/) (Workflow Automation)
-   **AI Model:** Google Gemini 1.5 Flash
-   **Database:** Google Sheets
-   **Interface:** Telegram Bot API

## ⚙️ How It Works

1.  **Trigger:** User sends a message or photo to the Telegram Bot.
2.  **Router:** n8n determines if the input is a text command, natural language, or an image.
3.  **Processing:**
    -   If **Image**: Gemini Vision analyzes the receipt.
    -   If **Text**: Gemini extracts entities (Item, Price, Category).
    -   If **Command**: n8n fetches data from Google Sheets.
4.  **Response:** The bot sends a formatted confirmation or report back to the user.

## 🔧 Setup & Installation

1.  Import the `finance-agent-workflow.json` file into your n8n instance.
2.  Set up the required credentials in n8n:
    -   Telegram Bot API Token
    -   Google Cloud Console (for Gemini API)
    -   Google Sheets OAuth2
3.  Create a Google Sheet with the following columns: `Toko`, `Total`, `Items`, `Tanggal`, `Waktu`.
4.  Activate the workflow!

## 📸 Screenshots

**The Automation Workflow:**
<img width="953" height="577" alt="image" src="https://github.com/user-attachments/assets/e14518ef-8439-4d14-a61e-6c6381002c1d" />


**Bot in Action:**
<img width="951" height="986" alt="image" src="https://github.com/user-attachments/assets/6f72a097-d3d5-463d-ae12-d99226047a01" />
<img width="959" height="984" alt="image" src="https://github.com/user-attachments/assets/c0ec0266-db3e-49fc-9c25-899b36246c36" />



---
*Created by [Nama Kamu]*
