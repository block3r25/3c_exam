# BSIT Exam App

A web-based examination application designed for **Bachelor of Science in Information Technology (BSIT)** students. The system provides a centralized platform for creating, managing, administering, and taking online examinations.

## 📌 Overview

The **BSIT Exam App** is designed to simplify the examination process for students, instructors, and administrators.

It provides functionality for:

* Student examination
* Question and question-bank management
* Examination creation and scheduling
* Automated scoring
* Examination result management
* Student performance monitoring
* User and access management
* Examination history and records

The application can be used for quizzes, periodic examinations, departmental assessments, mock examinations, and other academic assessments.

---

## ✨ Features

### 👨‍🎓 Student

* Student account authentication
* View available examinations
* Examination instructions
* Start and submit examinations
* Multiple-choice and other supported question types
* Countdown timer
* Automatic submission when time expires
* Question navigation
* Answer tracking
* Examination score
* Examination history
* Review of results, subject to instructor settings

### 👨‍🏫 Instructor / Faculty

* Create examinations
* Create and manage questions
* Organize questions by subject/topic
* Set examination duration
* Configure examination schedules
* Set passing scores
* Randomize questions
* Randomize answer choices
* Assign examinations to students/classes
* View student submissions
* View examination results
* Monitor student performance

### 👨‍💼 Administrator

* User management
* Student management
* Faculty/instructor management
* Subject management
* Course/program management
* Examination management
* Question-bank management
* System configuration
* Reports and statistics
* Access control

---

## 🛡️ Examination Security

The system may include several mechanisms to help maintain examination integrity:

* Authenticated user access
* Role-based access control
* Examination time limits
* Randomized questions
* Randomized answer choices
* One-attempt examination configuration
* Automatic submission
* Examination status tracking
* Secure answer storage
* Audit logging

> Security features should be configured according to the institution's examination policies and applicable privacy requirements.

---

## 🏗️ System Architecture

The application follows a web-based client-server architecture.

```text
+----------------------+
|      Student         |
|      Browser         |
+----------+-----------+
           |
           v
+----------------------+
|    BSIT Exam App     |
|    Web Application   |
+----------+-----------+
           |
           v
+----------------------+
|       Database       |
|   MySQL / MariaDB    |
+----------------------+
```

---

## 🗃️ Main Modules

### Authentication

Handles:

* Login
* Logout
* Password management
* Session management
* User roles
* Access permissions

### Examination Management

Handles:

* Examination creation
* Examination configuration
* Scheduling
* Instructions
* Duration
* Question assignment
* Examination status

### Question Bank

Handles:

* Question creation
* Question editing
* Question deletion
* Question categorization
* Correct answers
* Question difficulty
* Question randomization

### Examination Interface

Provides students with:

* Examination timer
* Question navigation
* Answer selection
* Progress indicator
* Submission confirmation
* Automatic submission

### Results

Provides:

* Individual examination scores
* Student results
* Class results
* Passing/failing status
* Examination statistics
* Performance summaries

### Reports

Possible reports include:

* Examination results
* Student performance
* Subject performance
* Question analysis
* Score distribution
* Examination participation

---

## 💻 Technology Stack

Update this section according to the technologies used in your implementation.

**Frontend**

* HTML5
* CSS3
* JavaScript
* Bootstrap 5
* jQuery
* DataTables

**Backend**

* PHP

**Database**

* MySQL / MariaDB

**Additional Libraries**

* SweetAlert
* AJAX
* Other libraries used by the project

---

## 📁 Suggested Project Structure

```text
bsit-exam-app/
│
├── assets/
│   ├── css/
│   ├── js/
│   ├── images/
│   └── plugins/
│
├── config/
│   └── database.php
│
├── admin/
│   ├── dashboard.php
│   ├── users/
│   ├── subjects/
│   ├── examinations/
│   └── questions/
│
├── faculty/
│   ├── dashboard.php
│   ├── examinations/
│   ├── questions/
│   └── results/
│
├── student/
│   ├── dashboard.php
│   ├── examinations/
│   ├── exam.php
│   └── results/
│
├── api/
│
├── includes/
│
├── uploads/
│
├── index.php
├── login.php
├── logout.php
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/bsit-exam-app.git
```

### 2. Enter the Project Directory

```bash
cd bsit-exam-app
```

### 3. Configure the Database

Create a MySQL/MariaDB database:

```sql
CREATE DATABASE bsit_exam;
```

Import the database schema provided in the project:

```text
database/bsit_exam.sql
```

### 4. Configure Database Connection

Update the database configuration according to your server:

```php
$host = "localhost";
$username = "root";
$password = "";
$database = "bsit_exam";
```

### 5. Configure the Web Server

Place the project inside your web server directory.

For example:

```text
htdocs/
└── bsit-exam-app/
```

For Apache:

```text
http://localhost/bsit-exam-app/
```

---

## 🔐 Default Accounts

If the project includes default accounts, document them here.

| Role          | Username | Password |
| ------------- | -------- | -------- |
| Administrator | admin    | ChangeMe |
| Faculty       | faculty  | ChangeMe |
| Student       | student  | ChangeMe |

> Change all default passwords before deploying the application to a production environment.

---

## 🔄 Examination Workflow

```text
Administrator
     │
     ├── Manage Users
     ├── Manage Subjects
     └── Manage System
             │
             ▼
          Faculty
             │
             ├── Create Questions
             ├── Create Examination
             ├── Set Schedule
             └── Assign Students
                     │
                     ▼
                  Student
                     │
                     ├── View Examination
                     ├── Start Exam
                     ├── Answer Questions
                     └── Submit
                           │
                           ▼
                       Evaluation
                           │
                           ▼
                        Results
```

---

## 📊 Examination Scoring

The system can automatically calculate examination scores based on the configured answer key.

Example:

```text
Total Questions: 50
Correct Answers: 42
Score: 42 / 50
Percentage: 84%
```

The scoring mechanism can be configured to support institutional grading policies.

---

## 🧑‍💻 Development

### Requirements

Recommended development environment:

* PHP 8.x
* MySQL 8.x / MariaDB 10.x
* Apache 2.4+
* Modern web browser
* Git

### Development Guidelines

When contributing code:

1. Follow the existing project structure.
2. Use prepared statements for database queries.
3. Validate and sanitize user input.
4. Avoid exposing database credentials.
5. Use appropriate access controls.
6. Test changes before committing.
7. Do not commit sensitive configuration files.

---

## 🔒 Security Considerations

Before deploying the application to production:

* Use HTTPS.
* Store passwords using secure password hashing.
* Use prepared SQL statements.
* Validate all user input.
* Implement CSRF protection.
* Implement appropriate session security.
* Restrict administrative functions.
* Protect uploaded files.
* Do not commit `.env` files or database credentials.
* Regularly back up the database.
* Maintain audit logs for important actions.

---

## 🔑 Environment Configuration

Sensitive configuration should not be committed to Git.

Example:

```text
.env
```

Example configuration:

```env
DB_HOST=localhost
DB_DATABASE=bsit_exam
DB_USERNAME=exam_user
DB_PASSWORD=your_secure_password
```

Add sensitive files to `.gitignore`:

```gitignore
.env
config/database.php
uploads/*
*.log
```

---

## 📝 Future Enhancements

Possible future improvements include:

* [ ] Question bank import/export
* [ ] Excel question import
* [ ] PDF examination reports
* [ ] Advanced examination analytics
* [ ] Question difficulty analysis
* [ ] Item analysis
* [ ] Random question pools
* [ ] Automatic certificate generation
* [ ] Email notifications
* [ ] Mobile-responsive examination interface
* [ ] Dark mode
* [ ] Examination activity logs
* [ ] Dashboard analytics
* [ ] LMS integration
* [ ] API integration
* [ ] QR-code examination access
* [ ] Enhanced anti-cheating controls

---

## 📜 License

This project is intended for academic and institutional use.

Specify your preferred license here, for example:

```text
MIT License
```

or

```text
Proprietary / Institutional Use
```

---

## 👨‍💻 Developer

**BSIT Exam App**

Developed for academic examination and assessment purposes.

---

## 📞 Support

For technical concerns, system issues, or feature requests, contact the project administrator or development team.

---

## ⭐ Project Status

**Status:** Active Development

The system is continuously being improved with additional examination, reporting, security, and administrative features.
