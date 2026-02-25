# Tax Companion
![Static Badge](https://img.shields.io/badge/vishnevvskaya-TaxCompanion-TaxCompanion)
![Python Version](https://img.shields.io/badge/Python-3.12.4-blue.svg)
![GAS Runtime](https://img.shields.io/badge/GAS-V8-green.svg)
[![Redis](https://img.shields.io/badge/Redis-6.2-red)](https://redis.io/)

> [!IMPORTANT]
> This project shows only the visual components of the bot in Telegram.

Is an accounting Telegram bot developed using [Aiogram](https://github.com/aiogram/aiogram), [Google Apps Script](https://developers.google.com/apps-script?hl=en) with Google Sheets integration and [Redis](https://redis.io/) for session management.

---

# Prerequisites

* Redis installed and running _(locally or remotely)_
* Google account _(to create the spreadsheet and script)_
* Telegram Bot Token _(obtain from [@BotFather](https://t.me/botfather))_

# Usage

Clone the repository:
```
git clone https://github.com/vishnevvskaya/tax-companion.git
cd tax-companion
```
Install the required modules:
```
pip install -r requirements.txt
```
Set up environment variables:
- Скопируйте файл `.example.env` в `.env`:
```
cp .example.env .env
```
- Edit the .env file and fill in your actual values (please use the complete configuration provided in the code as a guide)
  
---

# Running the bot
```
python main.py
```

# Setting up Google Sheets

The bot uses Google Sheets to store data. To set up the integration, follow these steps:

1. Create a new Google Sheets. Copy its ID from the URL (the part between /d/ and /edit).
2. Open Extensions -> Apps Script.
3. Copy the contents of the files from your repository's GAS/ folder (e.g., triggerController.gs) into the script editor.
4. Configure triggers: In the script editor, configure the necessary triggers (e.g., time-based backups).
5. Save and deploy the project. You may need the deployment ID to communicate with the bot.

> [!NOTE]
> To use the Google Sheets API from Python, you'll also need to set up a service account and grant it access to your spreadsheet. For more information, see the [Google Sheets API documentation](https://developers.google.com/sheets/api/guides/authorizing).

---

# Documentation

The user documentation can be obtained from [this link](https://github.com/vishnevvskaya/tax-companion/blob/main/index.md).