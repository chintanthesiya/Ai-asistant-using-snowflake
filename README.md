👨‍💻 About the Author

Hi, I'm Chintan Thesiya, a passionate Data Analyst Learner with a strong interest in Data Analytics, SQL, Python, Snowflake, Streamlit, Business Intelligence, and AI-powered Data Applications.
I enjoy building projects that transform raw data into interactive dashboards and intelligent applications. My goal is to continuously learn modern data technologies and apply them to solve real-world business problems.

This project demonstrates how to build a Rule-Based AI Assistant using Snowflake, Snowpark Python, SQL, Pandas, and Streamlit without relying on external AI APIs.
-----------Dashboard
![Dashboard](<img width="1037" height="656" alt="Screenshot 2026-06-27 114226" src="https://github.com/user-attachments/assets/cecdba5a-372f-4cea-bb82-a67a061dcb78" />
)

--------------AI Assistant Chat
![Chat](<img width="985" height="568" alt="Screenshot 2026-06-27 114335" src="https://github.com/user-attachments/assets/29f7d54d-47e9-4c60-bea2-43d31e00e451" />
)
![Chat](<img width="980" height="587" alt="Screenshot 2026-06-27 114401" src="https://github.com/user-attachments/assets/acac0bba-098c-4455-993a-a582b093d7f0" />
)
🤝 Let's Connect

I'm always open to connecting with fellow developers, data analysts, recruiters, and technology enthusiasts.

💼 LinkedIn: <https://www.linkedin.com/in/chintan-thesiya-6a9581321 >
💻 GitHub: <https://github.com/chintanthesiya/Ai-asistant-using-snowflake>
📧 Email: <chintanthesiya0142@gmail.com>

📊 US Economic AI Assistant using Snowflake Streamlit

A rule-based AI assistant built with Snowflake Streamlit, Snowpark Python, and SQL that answers questions about US economic indicators directly from a Snowflake database.

Unlike LLM-based chatbots, this project uses a rule-based query engine that converts user questions into SQL queries, retrieves live data from Snowflake, and returns concise, data-driven responses.

🚀 Project Overview

This project demonstrates how to build an AI-style assistant using only Snowflake technologies.

The assistant can answer questions such as:

What is the latest CPI?
What is the current unemployment rate?
Show the latest mortgage rate.
Show the unemployment trend.
Display the latest economic dashboard.

Instead of using an external AI model, the application detects user intent through predefined rules, executes SQL queries against Snowflake, and formats the results into natural-language responses.

🏗️ Project Workflow
Step 1 — Create a Snowflake Database

Create a new database.

CREATE DATABASE ECON_AGENT_DB;
Step 2 — Create a Schema
CREATE SCHEMA ANALYTICS;
Step 3 — Import Public Economic Data

Import economic datasets from the Snowflake Marketplace or Public Data Products.

Example data sources include:

Bureau of Labor Statistics (BLS)
Freddie Mac
US Economic Indicators

After importing, create a Dynamic Table that stores the required indicators.

Step 4 — Create the Dynamic Table

The project uses the following table.

ECON_AGENT_DB
    └── ANALYTICS
            └── ECONOMIC_DASHBOARD_LIVE

The table contains the following columns.

Column	Type
DATE	DATE
CPI	FLOAT
UNEMPLOYMENT_RATE	FLOAT
MORTGAGE_RATE_30Y	FLOAT
Step 5 — Data Filtering and Preparation

A Jupyter Notebook is used for data exploration and preprocessing.

Tasks include:

Loading economic datasets
Removing unnecessary columns
Selecting required indicators
Handling missing values
Validating data types
Preparing the final dataset
Uploading cleaned data into Snowflake

The notebook uses:

Python
Pandas
Snowpark Python
Step 6 — Build the Streamlit Application

The Streamlit application runs entirely inside Snowflake.

Responsibilities include:

Connecting to Snowflake
Loading economic data
Displaying KPI cards
Maintaining chat history
Detecting user intent
Executing SQL queries
Displaying charts
Returning AI-style responses
Step 7 — Rule-Based AI Engine

The application does not use an external LLM.

Instead, it follows this workflow.

User Question
       │
       ▼
Intent Detection
       │
       ▼
Rule Matching
       │
       ▼
Generate SQL Query
       │
       ▼
Execute Query in Snowflake
       │
       ▼
Retrieve Result
       │
       ▼
Generate Natural Language Response

Example:

User asks

What is the latest CPI?

The application generates

SELECT DATE,
       CPI
FROM ECON_AGENT_DB.ANALYTICS.ECONOMIC_DASHBOARD_LIVE
WHERE CPI IS NOT NULL
ORDER BY DATE DESC
LIMIT 1;

The SQL executes directly in Snowflake.

The application then formats the result as:

Latest CPI

Date: 2025-05-01

CPI: 321.47
📊 Supported Indicators
Consumer Price Index (CPI)
Unemployment Rate
30-Year Mortgage Rate
💬 Supported Questions

Users can ask questions such as:

Latest CPI
Current inflation
Latest unemployment rate
Show unemployment trend
Show inflation trend
Mortgage rate today
Latest mortgage rate
Economic dashboard
Show all indicators
Compare unemployment and inflation
Latest economic report
📁 Project Structure
US-Economic-AI-Assistant/

│
├── notebooks/
│     └── data_preprocessing.ipynb
│
├── streamlit/
│     └── app.py
│
├── sql/
│     ├── create_database.sql
│     ├── create_schema.sql
│     ├── create_dynamic_table.sql
│     └── queries.sql
│
├── images/
│
├── README.md
│
└── requirements.txt
📒 Jupyter Notebook Workflow

The notebook performs the following operations.

1. Connect to Snowflake

Using Snowpark Python.

2. Load Raw Economic Data

Read imported public datasets.

3. Clean the Data
Remove null values
Filter required columns
Standardize formats
4. Select Required Columns
DATE

CPI

UNEMPLOYMENT_RATE

MORTGAGE_RATE_30Y
5. Validate Data

Check:

Missing values
Data types
Duplicate records
6. Upload Processed Data

Write the cleaned dataset into

ECON_AGENT_DB.ANALYTICS.ECONOMIC_DASHBOARD_LIVE
🖥️ Streamlit Features
Interactive dashboard
Chat interface
KPI cards
Sidebar suggestions
Trend visualization
SQL execution
Rule-based AI
Session history
Cached queries
Direct Snowflake integration
⚙️ Technology Stack
Snowflake
Snowpark Python
Streamlit
SQL
Python
Pandas
📈 How It Works
Public Economic Data
          │
          ▼
Snowflake Marketplace
          │
          ▼
Dynamic Table
          │
          ▼
Data Cleaning (Pandas)
          │
          ▼
Snowflake Table
          │
          ▼
Snowpark
          │
          ▼
Rule Engine
          │
          ▼
SQL Query
          │
          ▼
Snowflake Execution
          │
          ▼
Result
          │
          ▼
AI Assistant Response
🎯 Future Improvements
Natural language intent expansion
Additional economic indicators
Date-range filtering
Interactive charts
Comparative economic analysis
Snowflake Cortex integration
Text-to-SQL capabilities
Automated trend summaries

------this actually boost your daily fetching data from cloude base database and you can massive data filter in few seconds  ------------------------
