# GEM IP Organizational Dashboard

This project generates a dynamic HTML dashboard that visualizes and summarizes key organizational insights from employee data. The dashboard supports stakeholder reporting and people analytics use cases by surfacing trends across job functions, roles, promotions, span of control, and tenure.

## Features

- Loads and merges employee snapshot and history datasets.
- Cleans and prepares structured HR data.
- Generates multiple interactive visualizations using Plotly.
- Conducts statistical comparisons (e.g., t-tests, chi-square tests).
- Automatically creates plain-language narrative insights.
- Renders a fully styled, standalone HTML dashboard using a Jinja2 template.
- Designed to align visually with Netflix-inspired branding.

## Inputs

- `employee_snapshot.csv`: Snapshot of current employee states, including job function, level, and reporting relationships.
- `employee_history.csv`: Historical data on each employee's hire date and promotion date.
- `gem_ip_template.html`: Custom HTML template used to layout the visual dashboard with integrated chart sections and insights.

## Outputs

- `gem_ip_dashboard.html`: A complete standalone HTML file that combines data visualizations, summaries, and narratives into a single dashboard view.

## How to Run

1. Ensure all required Python packages are installed. You can find the list in `REQUIREMENTS.md`.
2. Place the data files (`employee_snapshot.csv`, `employee_history.csv`) and the Jinja2 HTML template file (`gem_ip_template.html`) in the working directory.
3. Run the notebook in a Python environment such as Jupyter Notebook or Google Colab.
4. The script will generate visualizations, statistical summaries, and narrative insights and compile them into `gem_ip_dashboard.html`.
5. Open the generated HTML file in any modern browser to view and interact with the dashboard.

## Use Cases

- Organizational health assessments
- Executive-level HR reporting
- Fairness and equity review across promotions and leadership
- Internal data storytelling for People Analytics teams
