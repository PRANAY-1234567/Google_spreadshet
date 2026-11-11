# 📊 Google Sheets Manager Using Python

## 📌 About the Project

Google Sheets Manager is a Python-based project that allows users to work with Google Spreadsheets directly through Python code.

Instead of manually opening Google Sheets and entering data, you can use this program to create spreadsheets, add data, and read existing data automatically.

The project uses the Google Sheets API and OAuth 2.0 authentication to connect Python with your Google account.

## 🚀 Features

- **Google Authentication:** Connects to your Google account using OAuth 2.0.
- **Create Spreadsheet:** Creates a new Google Spreadsheet programmatically.
- **Add Data:** Inserts new rows of data into a spreadsheet.
- **Read Data:** Retrieves data from a spreadsheet or a selected range.
- **Token Management:** Saves authentication details locally to avoid logging in every time.
- **Automatic Token Refresh:** Refreshes expired access tokens when possible.
- **Reusable Python Class:** Uses an object-oriented approach to keep the code organised.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python 3 | Main programming language |
| Google Sheets API v4 | Connects Python with Google Sheets |
| google-auth | Handles authentication |
| google-auth-oauthlib | Manages OAuth 2.0 login |
| google-api-python-client | Sends requests to Google APIs |

## 📦 Installation and Setup

### Step 1: Clone the Repository

Open your terminal and run:

```bash
git clone https://github.com/your-username/google-sheets-manager.git
```

Move into the project directory:

```bash
cd google-sheets-manager
```

### Step 2: Install Required Libraries

Install the required Python packages:

```bash
pip install --upgrade google-api-python-client google-auth google-auth-oauthlib
```

### Step 3: Configure Google API

To connect your Python program with Google Sheets, you need OAuth 2.0 credentials.

1. Open the [Google Cloud Console](https://console.cloud.google.com/).
2. Create a new Google Cloud project.
3. Enable the Google Sheets API.
4. Configure the OAuth consent screen.
5. Create an OAuth 2.0 Client ID.
6. Download the credentials JSON file.
7. Place the downloaded file in your project folder.

Your project is now ready for Google authentication.

## 💻 How to Use

### 1. Create a Google Spreadsheet

Create an object of the `GoogleSheetsManager` class and call the `create_spreadsheet()` method.

```python
manager = GoogleSheetsManager()

spreadsheet_id = manager.create_spreadsheet("My First Sheet")

print(spreadsheet_id)
```

This creates a new spreadsheet in your Google account.

### 2. Add Data to Google Sheets

Use the `add_data()` method to insert rows into the spreadsheet.

```python
manager.add_data(["Name", "Age", "City"])

manager.add_data(["Pranay", "22", "Yavatmal"])
```

This adds the given information to your spreadsheet.

### 3. Read Data from Google Sheets

Use the `read_data()` method to retrieve the stored information.

```python
data = manager.read_data()

print(data)
```

The program reads the spreadsheet data and returns it in Python.

## 📂 Project Structure

```text
google-sheets-manager/
│
├── google_sheets_manager.py
├── client_secret.json
├── token.pickle
├── README.md
└── .gitignore
```

| File | Description |
|---|---|
| `google_sheets_manager.py` | Contains the Python class and Google Sheets operations. |
| `client_secret.json` | Stores OAuth 2.0 client credentials. |
| `token.pickle` | Stores authentication tokens for reuse. |
| `README.md` | Contains project information and setup instructions. |
| `.gitignore` | Prevents sensitive files from being uploaded to GitHub. |

## 🔐 Security

Google API credentials and authentication tokens contain sensitive information.

Never upload these files to a public GitHub repository.

Add the following entries to your `.gitignore` file:

```gitignore
client_secret.json
token.pickle
*.json
__pycache__/
```

## ⚙️ How It Works

The project follows these steps:

1. **Authentication:** Python connects to your Google account using OAuth 2.0.
2. **Token Storage:** Authentication tokens are saved locally for future use.
3. **API Connection:** The program connects to Google Sheets API v4.
4. **Spreadsheet Creation:** You can create a new spreadsheet using Python.
5. **Data Insertion:** You can add rows of information to the spreadsheet.
6. **Data Retrieval:** You can read existing spreadsheet data whenever required.

## ⚠️ Common Issues and Solutions

| Problem | Possible Solution |
|---|---|
| Authentication Error | Check your OAuth credentials and consent screen configuration. |
| Permission Denied | Make sure the Google Sheets API is enabled and the correct OAuth scopes are used. |
| Token Error | Delete the old `token.pickle` file and authenticate again. |
| API Error | Check your internet connection and API configuration. |
| Spreadsheet Not Found | Verify that the spreadsheet ID is correct. |

## 📌 Applications

This project can be used for:

- Automating data entry in Google Sheets.
- Storing application data.
- Generating reports automatically.
- Maintaining records and logs.
- Connecting Python applications with Google Sheets.
- Building simple data management systems.

## 👨‍💻 Author

**Pranay Vishwanath Jadhao**

Final-Year Electronics and Telecommunication Engineering Student

Aspiring Software Developer

GitHub: [Your GitHub Profile](https://github.com/your-username)

![Spreadsheet](https://github.com/user-attachments/assets/004206eb-db98-4bb0-bb5f-7a693cb663b2)

![spreadsheet 2](https://github.com/user-attachments/assets/20f8708c-3140-4716-89f3-d169866b6c49)
