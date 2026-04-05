# Life Expectancy Analyzer

This project combines public health and NGO-related data in a relational database and visualizes the results in a Streamlit dashboard to explore how drinking water access relates to life expectancy and infant mortality.

## Overview
- University group project for a database systems course
- Built around a decision-support use case for NGOs
- Combines data on life expectancy, drinking water access, infant mortality, and NGO support
- Final output: relational database, SQL queries and views, ETL pipeline, and interactive Streamlit dashboard

## What this folder contains
- `webapp.py`: Streamlit dashboard for interactive exploration
- `Transform_CSV.py`: ETL and data transformation script
- `Queries/`: SQL scripts for schema creation, loading, views, indexing, and user setup
- `streamlit/`: dashboard modules and supporting application code
- `img/`: selected screenshots and architecture diagrams
- `Bericht_DankDaten.pdf`: final technical report
- `requirements.txt`: Python dependencies

## Data and database design
- Public health data from WHO-related sources and Kaggle datasets
- Additional NGO support data for selected non-profit organizations
- Relational schema with entities for country, continent, life expectancy, drinking water supply, infant mortality, and organization
- Views used as the interface layer between the database and the dashboard

## Methods
- Extract, transform, and load workflow for CSV-based source data
- Relational modeling with primary and foreign keys
- SQL-based loading and view creation
- Streamlit dashboard connected to a MySQL database
- Performance checks using execution plans and indexing
- Basic role-based access design for admin, developer, and dashboard users

## Key findings
- The project found a positive correlation between drinking water access and life expectancy
- Countries with lower access to clean drinking water also tended to show higher infant mortality
- Interactive maps and scatterplots helped compare countries over time and identify regions with greater need
- NGO support was visualized to show country-level development trends over multiple years

## Tech stack
Python, MySQL, SQL, Streamlit, pandas

## Notes
- This folder is kept as part of my bachelor coursework archive
- The original project used a remote MySQL setup in a university lab environment
- Sensitive configuration files and credentials should not be published

## Project context
Group project for the Database Systems course during my bachelor studies.