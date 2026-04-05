# Air Quality and Office Performance Data Visualization

This project explores how indoor air quality metrics such as CO2, TVOC, and temperature relate to office conditions and perceived productivity through interactive visual storytelling.

## Overview
- University group project in data visualization
- Built around real air-Q sensor data from an architecture office
- Goal: communicate how indoor air quality may affect comfort, focus, and work performance
- Final outputs include an interactive HTML data story and written report

## What this folder contains
- `main.ipynb`: notebook used for cleaning, analysis, and visualization
- `main.html`: exported interactive data story
- `final_report.pdf`: final report
- `project_summary.pdf`: short project summary
- `csv/`: raw sensor data from multiple office spaces
- `img/`: floor plan and supporting images
- `requirements.txt`: Python dependencies

## Methods
- Cleaned and transformed raw air-Q sensor data
- Compared measurements across two office floors
- Used floor plans to contextualize sensor placement, plants, and workspaces
- Designed visualizations for time trends, comparisons, density, and distribution
- Built the final narrative with interactive Plotly charts and Quarto-based reporting

## Chart types used
- Line charts for time-based behavior and trends
- Heatmaps for quick visual summaries
- Comparison charts for office-to-office differences
- Distribution charts for value spread and outlier detection
- Area charts for comparing average intensity over time

## Data source
- Real-time data from air-Q sensors in an architecture office
- Additional floor plan images used to explain measurement locations

## Key findings
- Regularly opening windows was associated with lower CO2 and TVOC levels
- More plants appeared to have a positive effect on indoor air quality
- Continuous monitoring helps identify periods of poor air quality and supports better workplace conditions
- The project focused on communication and interpretation rather than causal proof

## Tech stack
Python, pandas, NumPy, Plotly, Quarto, Jupyter

## Notes
- This folder is kept as part of my bachelor coursework archive
- The project focuses on data storytelling and visualization, not predictive modeling
- The HTML and PDF outputs are the main deliverables

## Project context
Group project for a data visualization course during my bachelor studies.