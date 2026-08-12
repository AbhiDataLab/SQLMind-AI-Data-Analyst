# SQLMind AI — MySQL Data Analyst Agent

SQLMind AI is an AI-powered SQL Data Analyst built using n8n, Ollama, and MySQL.

## Project Overview

SQLMind allows users to ask questions about booking data in natural language.

The AI Agent:

1. Receives the user's question.
2. Generates a MySQL SELECT query.
3. Executes the query using the MySQL tool.
4. Uses the returned database result.
5. Provides a concise business-focused answer.
6. Shows the SQL query used.

## Technologies Used

- n8n
- Ollama
- Llama 3.2
- MySQL
- AI Agent
- SQL

## Database

The project uses the following table:

`cleaned_booking_data`

Important columns:

- Booking_ID
- Booking_Status
- Vehicle_Type
- Booking_Value
- Customer_Rating
- Driver_Ratings
- Ride_Distance

## Booking Status

- Canceled by Driver
- Success
- Canceled by Customer
- Driver Not Found

## Key Features

- Natural-language SQL analysis
- MySQL database querying
- SELECT-only SQL policy
- Controlled database schema
- Percentage calculations based on booking count
- Business-focused responses
- SQL query transparency
- Local AI using Ollama

## Workflow

```text
User
  ↓
n8n Chat Trigger
  ↓
AI Agent
  ↓
Ollama Llama 3.2
  ↓
MySQL SQL Tool
  ↓
Database Result
  ↓
Business Answer