# EmailSumAgent

**EmailSumAgent** is an agent that connects to your Gmail inbox, fetches unread emails from the last 24 hours, and summarizes them using Google's Gemini generative AI model. Summaries include the main topic, key points, and any required actions.

## Features

- Fetches unread emails from your Gmail inbox.
- Summarizes email content using Gemini AI.
- Displays sender, subject, and a concise summary for each email.
- Colorful terminal output for better readability.

## Requirements

- Python 3.8+
- Gmail account
- Google Cloud credentials for Gmail API and Gemini API

## Setup

1. **Clone the repository**  
   ```
   git clone <your-repo-url>
   cd EmailSumAgent
   ```

2. **Install dependencies**  
   ```
   pip install -r requirements.txt
   ```
   *(Create `requirements.txt` with the following if not present:)*  
   ```
   google-api-python-client
   google-auth-httplib2
   google-auth-oauthlib
   google-generativeai
   colorama
   ```

3. **Google API Credentials**  
   - Download your `credentials.json` from Google Cloud Console and place it in the project root.

4. **Set up environment variables**  
   - Create a `.env` file in the root directory:
     ```
     GOOGLE_API_KEY='your-gemini-api-key'
     ```

5. **Run the script**  
   ```
   python emailsum.py
   ```

   - On first run, a browser window will open to authenticate with your Google account.

## Usage

- The script will print summaries of your unread emails from the last 24 hours.
- Mark emails as read in Gmail to avoid repeat summaries.

## Security

- `.env`, `.vscode/`, and `credentials.json` are included in `.gitignore` to prevent accidental commits of sensitive data.

## License

MIT License

---

*Created by [Your Name].*
