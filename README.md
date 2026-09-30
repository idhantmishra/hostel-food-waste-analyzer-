Hostel Food Waste & Feedback Analyzer
Project ID: 03_HostelFoodWasteAnalyzer
A simple terminal app to keep track of meals made each day whats left over. How happy students are with the food in university hostels. It helps student mess groups and kitchen staff find dishes that get thrown away a lot take notes on how students feel about the food and make food when needed.

This app is made using the basic Python tools you get with Python and doesn't need any extra programs.

Overview
In hostels lots of food gets thrown away every day because meals are made in large batches without thinking about what students like. Things like paper notes don't work because they are not looked at and don't include what students think.

This project gives a offline system that checks how much food is wasted sorts the waste into levels (low moderate high) sends warnings for meals that have more than 20% waste and saves the records in a small computer database.

Features
Daily Meal Records: Enter the time of day (breakfast, lunch, snacks, dinner) dish name, amount made (in kg) amount wasted (in kg) and student ratings from 1.0 to 5.0.

Waste Calculations: Figures out the waste percentage using (wasted kg divided by prepared kg) multiplied by 100.

Waste Levels:

LOW (<10%): Normal bits left on plates and kitchen scraps.

10-20%): More leftovers that need changes to how much is made.

HIGH (>20% Critical Alert): Sends a red alert with ideas on what to do.

Reason for Waste Notes: Figures out if much food is thrown away because students don't like it (rating under 2.5) or because too much was made (rating 2.5 or higher).

Local Database: Saves the data in a database file called mess_waste.db that works on its own.

Checks for Problems: Makes sure numbers make sense (no weights, no more wasted than made and proper ratings).

Quick Test Mode: Comes with 10 Indian hostel dishes (Rajma Chawal Upma Soya Curry Lauki Paneer Masala) for testing.

Technologies & Tools Used
Language: Python 3 (version 3.8 or higher)

Database: SQLite3 (included in Python)

Testing Tools: unittest (included in Python)

No Extra Programs Needed: No need to download anything no pandas, flask, numpy or tabulate).

Screenshots


Mess Food Waste Dashboard

Steps to Install & Run
1. Requirements
Make sure you have Python 3.8 or newer installed:

python --version
2. Start the App
Go to the project folder. Start the app:

python main.py
(On Windows you can also use py main.py)

3. Try the Demo
To see sample hostel food data and results without entering anything:

python main.py --demo
How to Test
The project has a test system with 24 tests that check math functions, edge cases, database rules and how the system works in the terminal:

python -m unittest discover tests -v
All 24 tests finish in 0.01 seconds.

Project Layout

03_HostelFoodWasteAnalyzer/

├── main.py                  # Where the app starts ( menu and --demo option)

├── requirements.txt         # No extra programs needed

├── LICENSE                  # MIT License (Copyright 2026 Aryan Raj)

├── Statement.md             # What the project is about and its goals

├── README.md                # How to use the app and get started

├── mess_waste.db            # Database file (creates

├── waste_tracker/

│   ├── __init__.py          # Sets up the package

│   ├── analytics.py         # Does the math for waste percentages

│   ├── database.py          # Connects to the database. Manages data

│   └── cli.py               # Handles the terminal menu and reports

├── tests/

│   ├── __init__.py

│   ├── test_analytics.py    # Tests the math and edge cases

│   ├── test_database.py     # Tests the database and rules

│   └── test_cli.py          # Tests the inputs and outputs

├── screenshots/

│   ├── 01_dashboard.png     # Screenshot of the dashboard

│   └── README.md            # How to recreate the screenshot

└── docs/

├── PROJECT_REPORT.md    # 15-point academic evaluation report

├── PROJECT_REPORT.html  # Styled version of the report

└── PROJECT_REPORT.pdf   # Professional version of the report

Developer
Name: Idhant Mishra 

Student ID / Roll No: 26MIP10079

Course: Introduction, to Problem Solving and Programming (CSE1021)

Institution: VIT (VITyarthi Project Submission)
