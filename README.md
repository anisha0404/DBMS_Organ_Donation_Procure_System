🏥 Organ Donation Procure System

This is a DBMS-based web application developed using **Flask** and **MySQL**, designed to manage and streamline the process of **organ donation and procurement**. It supports hospitals, doctors, and administrators in registering donors, processing recipient requests, and maintaining a transparent transaction system — with automated triggers to log every critical operation.

---

📌 Features

👤 Admin
- Secure login access
- View and manage registered users
- Monitor donor–patient transactions
- Review system activity logs via triggers

🧑‍⚕️ Hospital/Doctor Staff
- Register donors and patients
- Submit organ procurement requests
- View organ availability
- Track donation and transplant transactions

📋 Logging System (via MySQL Triggers)
- All `INSERT`, `UPDATE`, and `DELETE` actions on `Donor`, `Patient`, and `Transaction` tables are automatically logged in the `log` table using **MySQL triggers**

---

🧱 Database Design

🔐 Tables Overview:
- `login`: Admin login credentials  
- `User`: Base info for both donors and patients  
- `User_phone_no`: Contact number for users  
- `Organization`: Hospitals or organ centers  
- `Doctor`: Doctor info linked to organizations  
- `Patient`: Organ requests by patients  
- `Donor`: Donor info and organ donations  
- `Organ_available`: Auto-generated available organ list  
- `Transaction`: Tracks donor-to-patient organ assignments  
- `Organization_phone_no` / `Doctor_phone_no`: Contact info  
- `Organization_head`: Management info  
- `log`: Records all critical DB operations triggered by events

 🔁 Triggers Included:
- `ADD_DONOR_LOG`, `UPD_DONOR_LOG`, `DEL_DONOR_LOG`  
- `ADD_PATIENT_LOG`, `UPD_PATIENT_LOG`, `DEL_PATIENT_LOG`  
- `ADD_TRASACTION_LOG`

---

💻 Tech Stack

| Layer     | Technology                |
|-----------|---------------------------|
| Backend   | Flask (Python)            |
| Frontend  | HTML, CSS (Bootstrap optional) |
| Database  | MySQL (MySQL Workbench)   |
| Charts    | matplotlib (optional usage) |

---

🚀 Getting Started

🔧 Prerequisites
- Python 3.x
- MySQL Server & MySQL Workbench
- Python libraries:
  ```bash
  pip install flask mysql-connector-python matplotlib

🔧 Setup Instructions

📥 Clone this repository
```bash
git clone https://github.com/your-username/dbms-project.git
cd dbms-project

Create virtual environment:
bash
Copy
Edit
python -m venv venv
venv\Scripts\activate

Install dependencies:
bash
Copy
Edit
pip install -r requirements.txt

🗄️ Set up the MySQL database
Open MySQL Workbench

Run the full SQL script to create the DBMS_PROJECT schema and tables

🗄️Default admin login is already inserted:
sql
Copy
Edit
INSERT INTO login VALUES ('admin','admin');

▶️Run the Flask app
bash
Copy
Edit
python main.py

🌐 Open in your browser
text
Copy
Edit
http://127.0.0.1:5000/

📊 Future Improvements
Role-based registration portal (Donor, Hospital)

Analytics dashboard with organ availability stats

Automatic organ matching suggestions

Secure password encryption (using SHA-256 or bcrypt)

REST API endpoints for integration with hospital systems

🙌 Developed By
Anisha Mehta
Computer Science Undergraduate
DBMS Mini Project — Organ Donation System
