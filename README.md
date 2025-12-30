![Spreadsheet](https://github.com/user-attachments/assets/004206eb-db98-4bb0-bb5f-7a693cb663b2)
![spreadsheet 2](https://github.com/user-attachments/assets/20f8708c-3140-4716-89f3-d169866b6c49)
📊 Google Sheets Manager using Python

This project provides a Python class to authenticate with the Google Sheets API and perform common operations such as:

Authenticating using OAuth 2.0

Creating a new Google Spreadsheet

Adding data (rows) to a spreadsheet

Reading data from a spreadsheet

It is useful for automation, data logging, reporting, and backend integrations.

🚀 Features

OAuth 2.0 authentication with token reuse

Automatic token refresh

Create Google Sheets programmatically

Append rows of data

Read data from any sheet range

Clean object-oriented design

🛠️ Technologies Used

Python 3

Google Sheets API v4

google-auth

google-auth-oauthlib

google-api-python-client

📦 Installation
1️⃣ Clone the repository
git clone https://github.com/your-username/google-sheets-manager.git
cd google-sheets-manager

2️⃣ Install dependencies
pip install --upgrade google-api-python-client google-auth google-auth-oauthlib

🔐 Google API Setup

Go to Google Cloud Console

Create a new project

Enable Google Sheets API

Create OAuth 2.0 Client ID

Download the credentials JSON file

Rename it (or keep the same name) and place it in the project root

⚠️ Important:
Do NOT upload your client secret JSON or token.pickle to GitHub.

Add them to .gitignore:

token.pickle
*.json

▶️ Usage
Create a Spreadsheet
manager = GoogleSheetsManager()
spreadsheet_id = manager.create_spreadsheet("My First Sheet")

Add Data
manager.add_data(["Name", "Age", "City"])
manager.add_data(["Pranay", "22", "Yavatmal"])

Read Data
data = manager.read_data()
print(data)

📂 Project Structure
├── google_sheets_manager.py
├── token.pickle
├── client_secret.json
├── README.md

🧠 How It Works (Brief)

Uses OAuth 2.0 for secure authentication

Stores access tokens locally (token.pickle)

Automatically refreshes expired tokens

Uses Google Sheets API v4 for operations

⚠️ Common Issues

Authentication Error

Ensure correct OAuth credentials

Delete token.pickle and re-authenticate

Permission Denied

Make sure Google Sheets API is enabled

Use correct OAuth scopes

📌 Use Cases

Data automation

Logging application data

Report generation

Backend integrations

Student projects & mini projects

👤 Author

Pranay Vishwanath Jadhao
Final Year – Electronics & Telecommunication
Aspiring Software Developer
