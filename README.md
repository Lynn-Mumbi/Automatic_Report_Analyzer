Overview
This Python script automates the analysis of MiX Telematics raw fleet reports, producing a structured, multi-sheet Excel report with visual insights into driver behavior, violations, and asset utilization.

The script is designed to support fleet managers, operations teams, and safety analysts in quickly understanding performance trends, identifying high-risk drivers, and measuring asset productivity.

 key Features
 1. RAG Driver Performance Report
Classifies each driver or vehicle into Red, Amber, or Green (RAG) zones based on the total number of violations recorded in the month:

Green: 0–20 violations

Amber: 21–40 violations

Red: 41+ violations

Calculates the percentage of drivers in each performance band.

Helps management quickly identify risk concentration in the fleet.

2. Top 3 Violators per Violation Type
Highlights the top 3 drivers or vehicles for each violation category.

Uses the most relevant metric for each type:

e.g., Overspeeding → ranked by distance over speed limit.

e.g., Harsh Braking / Acceleration → ranked by occurrence count.

Includes brief descriptions of each violation type for clarity and training purposes.

3. Violation Summary & Normalization
Calculates violation rate per 100 km for each type, normalized to fleet distance.

Color-codes each violation by severity:

Green = lowest rate

Red = highest rate

Highlights which behaviors are most prevalent and need intervention.

4. Daily Asset Utilization Sheet
Analyzes daily distance covered per vehicle throughout the month.

Color-codes each cell:

Green = >100 km (well utilized)

Amber = moderate usage

Red = low or zero usage

Helps assess underutilization or idle assets.
Output
The script generates a multi-sheet Excel workbook with the following tabs:

Sheet Name:	Description
RAG Report:	Driver risk categorization + summary stats
Top Violators:	Top 3 drivers/vehicles per violation type
Violation Summary:	Normalized per-100km violation rates + heat coloring
Utilization:	Daily per-vehicle distance with usage heat map

🛠 Requirements
Python 3.7+

Libraries: pandas, openpyxl, numpy, xlsxwriter (optional, for advanced formatting)

Install with:
bash
Copy
Edit
pip install pandas openpyxl numpy xlsxwriter

Benefits
Converts raw MiX data into management-ready insights.

Highlights drivers needing coaching or investigation.

Tracks vehicle usage patterns across the month.

Promotes proactive safety and operational decisions.
