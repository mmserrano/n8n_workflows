# Send Ebooks from Telegram to Kindle Workflow

## Overview
This n8n workflow automates the process of sending ebooks received via Telegram directly to your Kindle device. It uses the Telegram API to monitor messages and the Kindle email service to send documents seamlessly.

## Prerequisites
- An active Telegram account.
- A Kindle account with an associated email address.
- n8n installed and running on your local machine or server.
- Basic knowledge of how to create a Telegram bot.

## Setup Instructions

### Step 1: Create a Telegram Bot
1. Open Telegram and search for the BotFather.
2. Start a chat with BotFather and use the command `/newbot`.
3. Follow the prompts to name your bot and get your bot token.
4. Save the bot token as you will need it later.

### Step 2: Get Your Chat ID
1. Start a chat with your newly created bot.
2. Send any message to the bot.
3. Use the following URL in your browser to get your chat ID:
   ```
   https://api.telegram.org/bot<YOUR_BOT_TOKEN>/getUpdates
   ```
   Replace `<YOUR_BOT_TOKEN>` with the token you received from BotFather. Look for the `chat` object in the JSON response to find your chat ID.

### Step 3: Configure Google SpreadSheet
1. Create a new Google Spreadsheet called "Telegram Bot enviar a kindle" (or any other name to be added later in workflow).
2- The sheet "Hoja 1" must have columns "ID Telegram" and "Email Kindle".

### Step 4: Prepare the n8n Workflow
1. Clone the repository or download the `Telegram_send_to_kindle.json` file.
   ```bash
   git clone <repository-url>
   cd n8n_workflows/Send ebooks from Telegram to Kindle
   ```

2. Import the Workflow:
   - Open n8n in your browser.
   - Click on "Import" and upload the `Telegram_send_to_kindle.json` file.

3. Configure the Workflow:
   - Open the imported workflow in n8n.
   - Setup your credentials
   - Locate the following nodes and replace with your information: 
        - Telegram2: replace your-email-address with the gmail account you will send emails from
        - "Telegram5", "Telegram6", "Telegram8", "ErrorHandler": replace your-telegram-account by your telegram account's username or email, as you prefer to be contacted.

### Step 5: Activate the Workflow
- Once configured, activate the workflow to start monitoring Telegram messages.

## Usage
- The workflow will automatically trigger when a new message is received in the specified Telegram chat.
- If the message contains an ebook file, it will be sent to your Kindle email address.

## Troubleshooting
- Ensure that your Telegram bot token and chat ID are correct.
- Check that your Kindle email is properly set up to receive documents.
- Review n8n logs for any errors during execution.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing
Feel free to submit issues or pull requests for improvements or bug fixes.

## Contact
For any questions or support, please reach out to `contacto@aiflow.es`.