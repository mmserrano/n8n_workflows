# Lead Generation from Google Maps Workflow

## Overview
This n8n workflow automates the process of extracting business email addresses from Google Maps search results. It uses AI to generate targeted search queries and scrapes contact information from business websites listed on Google Maps.

## Prerequisites
- n8n installed and running on your local machine or server
- Google account for storing results in Google Sheets
- Google Cloud Platform account with Gemini API access
- SMTP server for sending results via email

## Setup Instructions

### Step 1: Configure Google Services
1. Set up a Google Cloud Project and obtain Gemini API credentials
2. Create a Google Sheet for storing the scraped emails
3. Configure Google Drive API access for downloading results

### Step 2: Configure Email Settings
1. Set up SMTP credentials in n8n
2. Update the email settings in the "Send email" node with your sending address

### Step 3: Prepare the n8n Workflow
1. Clone the repository or download the `Leads from Google Maps.json` file
   ```bash
   git clone <repository-url>
   cd n8n_workflows/Get lead emails from Google Maps
   ```

2. Import the Workflow:
   - Open n8n in your browser
   - Click on "Import" and upload the `Leads from Google Maps.json` file

3. Configure the Workflow:
   - Set up Google Sheets credentials
   - Configure Google Drive credentials
   - Add your Gemini API key
   - Update SMTP settings

## Usage
1. Access the provided form URL to start a new search
2. Enter the following information:
   - Type of business (e.g., dentist, lawyer, restaurant)
   - Location (e.g., Barcelona, Madrid)
   - Your email address to receive results
3. Submit the form to start the scraping process
4. Results will be:
   - Saved to Google Sheets
   - Sent to your email as a CSV file
   - Stored in Google Drive for backup

## Features
- AI-powered search query generation using Google Gemini
- Automatic website scanning for email addresses
- Duplicate email removal
- Results export in CSV format
- Automated email delivery of results
- Google Sheets integration for data storage

## Troubleshooting
- Ensure all Google API credentials are properly configured
- Verify SMTP settings if emails are not being received
- Check Google Sheets permissions if data is not being saved

## License
This project is licensed under the MIT License - see the [LICENSE](../LICENSE) file for details.

## Contributing
Feel free to submit issues or pull requests for improvements or bug fixes.

## Contact
For any questions or support, please reach out to `contacto@aiflow.es`.