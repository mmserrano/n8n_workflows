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

### Step 3: Configure Your Kindle Email
1. Log in to your Kindle account.
2. Go to your Amazon account settings and find the "Manage Your Content and Devices" section.
3. Under the "Preferences" tab, locate your Kindle email address (e.g., `yourname@kindle.com`).
4. Ensure that your Kindle email is set to receive documents from your Telegram bot's email.

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
   - Locate the Telegram node and replace the following placeholders:
     - **Bot Token**: `replace-me` (your bot token from BotFather)
     - **Chat ID**: `replace-me` (your chat ID obtained from the previous step)
   - Locate the Kindle node and replace the following placeholders:
     - **Kindle Email**: `replace-me` (your Kindle email address)
     - **Subject**: `replace-me` (e.g., "New Ebook from Telegram")
     - **Body**: `replace-me` (e.g., "Here is your ebook!")

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