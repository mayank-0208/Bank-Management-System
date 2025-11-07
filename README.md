# 🏦 Bank Management System (Python + Streamlit)
#📘 Overview
This is a Bank Management System Web App built using Python, Streamlit, and Object-Oriented Programming (OOP) concepts.
It allows users to create and manage bank accounts with features like account creation, deposit, withdrawal, balance check, update, and deletion — all through a clean, interactive web interface.

The project demonstrates how data persistence, OOP design, and frontend integration work together to build a fully functional mini banking system.

##🚀 Features

###🧾 1. Create New Account

Allows users to create a new account by entering their Name, Age, Email, and a 4-digit PIN.

The system automatically generates a unique Account Number using random alphanumeric combinations.

Validation ensures only users aged 18+ can open an account, and PINs must be 4 digits.

###💰 2. Deposit Money

Securely deposit an amount (up to ₹10,000 per transaction).

PIN verification ensures only valid account holders can perform deposits.

The balance is updated and saved in the local data.json database.

💸 3. Withdraw Money

Allows account holders to withdraw funds after verifying Account Number and PIN.

Prevents overdrawing — withdrawal is allowed only if sufficient balance exists.

Automatically updates the remaining balance in the data file.

📋 4. Show Account Details

Users can view their full account details after successful verification.

Information includes Name, Email, Age, Account Number, and Current Balance.

Uses Streamlit’s st.json() for neat, formatted output.

🧑‍💻 5. Update Account Information

Users can update their Name, Email, or PIN easily.

Keeps data consistent and ensures changes are saved immediately to data.json.

🗑️ 6. Delete Account

Allows secure account deletion by verifying the Account Number and PIN.

Permanently removes the user record from the system.

🧠 Tech Stack
Component	Technology Used
Frontend	Streamlit
Backend	Python (OOP-based)
Data Storage	JSON File
IDE	VS Code / PyCharm
Version Control	Git & GitHub
🧩 Project Structure
📦 Bank-Management-System
├── app.py              # Streamlit frontend
├── hello.py            # Bank class backend logic
├── data.json           # JSON database (auto-generated)
├── README.md           # Project documentation
└── requirements.txt    # Python dependencies (optional)

⚙️ How It Works (Step-by-Step)
1️⃣ User Interface

The app launches with a Streamlit sidebar menu offering options like Create Account, Deposit, Withdraw, etc.

Each option dynamically loads a form where the user can input data.

2️⃣ Backend (hello.py)

All operations are handled through the Bank class.

The class uses:

load_data() to read user records from data.json

save_data() to persist changes

OOP methods for each operation:

create_account(), deposit(), withdraw(), update_user(), delete_user()

3️⃣ Data Persistence

The app stores all data locally in data.json.

Every time a transaction occurs, the file updates instantly using json.dump().

4️⃣ Security

Every transaction and update is PIN-protected.

Account numbers are unique and randomly generated.

Sensitive inputs (like PINs) are masked in the Streamlit UI.

🖥️ How to Run the Project
Step 1: Clone the Repository
git clone git@github.com:your-username/Bank-Management-System.git
cd Bank-Management-System

Step 2: Install Required Packages
pip install streamlit


(Optional: You can also add a requirements.txt file and run pip install -r requirements.txt)

Step 3: Run the Streamlit App
streamlit run app.py

Step 4: Access in Browser

Visit 👉 http://localhost:8501

📘 Example Usage
🧍 Create Account
Field	Example
Name	Rohan Sharma
Age	22
Email	rohan123@gmail.com

PIN	1234

Output:

✅ Account created successfully  
ℹ️ Your Account Number: x7A2#3

💵 Deposit Money

Enter account number, PIN, and amount:

✅ Deposit successful

🧾 Show Account Details

Displays all saved details neatly as JSON.

📂 Data Example (data.json)
[
    {
        "name": "Rohan Sharma",
        "age": 22,
        "email": "rohan123@gmail.com",
        "pin": 1234,
        "accountNo.": "x7A2#3",
        "balance": 1000
    }
]

🔐 Validation Rules

Age must be 18 or above

PIN must be 4 digits

Deposit limit: 1 to 10,000

Withdrawal: Only if balance ≥ amount

🧠 Concepts Demonstrated

Object-Oriented Programming (OOP) in Python

File Handling & JSON data management

Frontend development using Streamlit

Data validation and error handling

Integration of UI with business logic

🧰 Tools Used

Python, Streamlit, JSON, VS Code, Git, GitHub

🌟 Future Enhancements

✅ Add login/signup with password hashing (bcrypt)

✅ Use SQLite or MongoDB instead of JSON

✅ Add transaction history logs

✅ Deploy on Streamlit Cloud or Render
