# 📎 Gmail Attachment Downloader

A simple Python-based tool that allows users to search their Gmail inbox and download attachments from matching emails.

The application uses the Gmail API through **EZGmail** and authenticates users securely using **Google OAuth 2.0**.

---

## ✨ Features

- 🔍 Search Gmail using Gmail search queries
- 📎 Automatically finds emails containing attachments
- 📋 Displays the subject of matching emails
- ⬇️ Downloads attachments from matching emails
- 🔐 Google OAuth 2.0 authentication
- 💻 Simple command-line interface
- 🛡️ Authentication files are excluded from Git

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| Python 3.11 | Application development |
| EZGmail | Gmail interaction |
| Gmail API | Access Gmail messages and attachments |
| Google OAuth 2.0 | User authentication |
| Git & GitHub | Version control and project hosting |

---

## 📂 Project Structure

```text
Attachment-Downloader/
│
├── .gitignore
├── README.md
│
└── Attachment_Downloader/
    └── attachment.py
Authentication Files

The following files are created locally but are not uploaded to GitHub:

credentials.json
token.json

These files contain authentication-related information and are protected using .gitignore.

⚙️ Requirements

Before running this project, make sure you have:

Python 3.10 or later
A Google account
Gmail API enabled
A Google Cloud project
Google OAuth 2.0 Desktop credentials
Internet connection
📦 Installation
1. Clone the Repository
git clone https://github.com/RaavanHrishi07/Attachment-Downloader.git

Navigate into the project:

cd Attachment-Downloader
2. Create a Virtual Environment

On Windows:

python -m venv venv

Activate the virtual environment:

.\venv\Scripts\activate
3. Install EZGmail

Install the required Python package:

pip install ezgmail
🔐 Google Cloud & Gmail API Setup

This project requires access to the Gmail API.

Step 1 — Create a Google Cloud Project

Create a new project using Google Cloud Console.

Step 2 — Enable Gmail API

Enable the Gmail API for your Google Cloud project.

Step 3 — Configure Google Auth Platform

Configure the OAuth consent screen using Google Auth Platform.

For a personal Gmail account, configure the application as an external application.

Step 4 — Create OAuth Client

Create an OAuth 2.0 client with:

Application Type: Desktop App
Step 5 — Download Credentials

Download the OAuth client JSON file and rename it:

credentials.json

Place the file inside:

Attachment_Downloader/
Step 6 — Add a Test User

If the application is in Testing mode, add the Gmail account that will be used to authenticate the application under:

Google Auth Platform → Audience → Test users

Never share your credentials.json file publicly.

▶️ Running the Application

Navigate to the application directory:

cd Attachment_Downloader

Run the application:

python attachment.py

The application will ask for a search query:

Enter search query:

Enter any Gmail search term.

For example:

invoice

The program automatically adds:

has:attachment

to the search query.

Therefore, the final Gmail search becomes:

invoice has:attachment

🔎 Example Usage
Enter search query: invoice

Result(s) with attachments:

Email Subject: Your Invoice
Email Subject: Monthly Invoice
Email Subject: Rapido Invoice
Email Subject: Your Tickets

Do you want to download attachment(s) in result(s) (Yes/No)?

Enter:

Yes

to download the attachments.

Enter:

No

to exit without downloading.

🔍 Gmail Search Queries

Because the application uses Gmail search syntax, you can use different Gmail search operators.

Search by sender
from:example@gmail.com
Search by subject
subject:invoice
Search for PDFs
filename:pdf
Search for a specific sender with invoices
from:example@gmail.com invoice

The application automatically adds:

has:attachment

to these queries.

📥 How Attachments Are Downloaded

The application:

Accepts a Gmail search query.
Adds the has:attachment filter.
Searches Gmail for matching conversations.
Displays the subjects of matching emails.
Asks the user whether attachments should be downloaded.
Downloads the attachments when the user confirms.
🔒 Security

Authentication files are intentionally excluded from this repository.

The following files should never be uploaded to GitHub:

credentials.json
token.json

They are excluded using .gitignore.

Do not share OAuth credentials, tokens, or other authentication information publicly.

🚨 Troubleshooting
ModuleNotFoundError: No module named 'ezgmail'

Install EZGmail:

pip install ezgmail
Can't find credentials file

Make sure the file is named exactly:

credentials.json

and is located inside:

Attachment_Downloader/

Make sure it is not accidentally named:

credentials.json.json
Access blocked: App has not completed verification

If the application is in Testing mode, make sure your Google account has been added under:

Google Auth Platform → Audience → Test users
Authentication

The first time the application is run, Google OAuth authentication will open in the browser.

After successful authentication, a local:

token.json

file may be created automatically.

🚀 Future Improvements

Planned improvements for future versions:

🖥️ Add a graphical user interface
📁 Allow users to choose a custom download directory
📎 Display attachment names and file sizes
☑️ Allow users to select individual emails
☑️ Allow users to select specific attachments
📊 Add download progress indicators
⚡ Improve batch downloading
🛑 Improve error handling
🔎 Add advanced search filters
📝 Add detailed logging
🎯 Project Purpose

The purpose of this project is to simplify the process of finding and downloading Gmail attachments.

Instead of manually opening multiple emails and downloading files one by one, users can search their inbox using Gmail search queries and download attachments from the matching results.

👨‍💻 Author

Hrishikesh Sharma

GitHub:
https://github.com/RaavanHrishi07

⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.

📄 License

This project is intended for educational and personal use.