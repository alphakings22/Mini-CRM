# Mini-CRM — Sales Pipeline

A contact and sales opportunity (deal) management application, with a sales pipeline and a tracking dashboard.

## Installation

pip install -r requirements.txt


## Run the application

streamlit run app.py


A SQLite database (`crm.db`) is created automatically on first launch, in the same folder. Data is saved locally.

## Features

* **Contacts**: add, view, and delete clients/prospects
* **Deals**: create sales opportunities linked to a contact, with a value and a stage (Prospect → Qualification → Negotiation → Won/Lost)
* **Dashboard**: total and active pipeline value, won value, conversion rate, and deal breakdown by stage

## Structure

mini-crm/
├── app.py Streamlit interface (3 tabs)
├── database.py SQLite data access layer (CRUD)
├── crm_analysis.py calculations and aggregations for the dashboard
├── requirements.txt
└── crm.db created automatically on first launch


## Possible next steps

Developed by Johnson Kwueku Bentsi Jucal

* Add an expected close date per deal, with automatic reminders
* CSV export of the pipeline
* Stage change history (audit trail)
