# SQLMind AI – MySQL Data Analyst Agent

SQLMind AI is an AI-powered MySQL Data Analyst Agent built with **n8n, Ollama, and MySQL**.

It allows users to ask business/data questions in natural language. The AI Agent converts the question into a valid MySQL `SELECT` query, executes it against the booking database, and returns the result in a simple business-friendly format.

---

## Project Overview

SQLMind AI is designed to make database analysis easier without requiring the user to manually write SQL queries.

### Example

User:

> What percentage of bookings were canceled by drivers?

SQLMind AI generates a MySQL query, executes it against the database, and returns the calculated result.

---

##  Architecture

The workflow contains three main components:

text

User
  ↓
n8n Chat Trigger
  ↓
AI Agent
  ↓
Ollama LLM
  ↓
MySQL Query Tool
  ↓
MySQL Database
  ↓
SQL Result
  ↓
Business-Friendly Answer

Technologies Used

n8n – AI workflow automation
Ollama – Local Large Language Model
Llama 3.2 – AI model
MySQL – Database
SQL – Data analysis
JSON – n8n workflow configuration

 Database

The project uses a MySQL table called:

cleaned_booking_data

Important columns include:

Booking_ID
Booking_Status
Vehicle_Type
Booking_Value
Customer_Rating
Driver_Ratings
Ride_Distance

Booking Status Values

The agent is configured to recognize:

Canceled by Driver
Success
Canceled by Customer
Driver Not Found

AI Agent Capabilities

SQLMind AI can answer questions such as:

What is the total number of bookings?
What is the total booking value?
Which vehicle type has the highest bookings?
What percentage of bookings were canceled by drivers?
What is the average customer rating?
What is the average driver rating?
What is the average ride distance?
How many successful bookings were completed?

The agent generates SQL based on the user's question and executes the query through the MySQL too
Setup
1. Install n8n

Install and run n8n locally.

2. Install Ollama

Install Ollama and download the required model:

llama3.2
3. Setup MySQL

Create a MySQL database and import the cleaned_booking_data table.

4. Configure MySQL in n8n

Create a MySQL credential in n8n and connect it to the MySQL Query Tool.

5. Configure Ollama

Connect the Ollama Chat Model to the AI Agent.

6. Import the Workflow

Import:

workflow/sqlmind-workflow-public.json

into n8n.

 Security Note

The workflow is designed to use a local MySQL database and local Ollama model.

Do not commit:

Database passwords
API keys
.env files
Private credentials
Production database connection details

Author

AbhiDataLab

Data Analyst | SQL | Python | Power BI | AI Automation

 Future Improvements

Planned improvements include:

Support for more datasets
Automatic business insight generation
Power BI integration
Dashboard generation
More advanced SQL validation
Query performance optimization
Support for additional LLMs
