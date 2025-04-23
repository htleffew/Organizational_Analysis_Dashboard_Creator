# Project Walkthrough: GEM IP Organizational Dashboard

This walkthrough explains each key component of the project notebook. The goal is to help users understand what each part of the code does and how it contributes to the final dashboard.

## 1. Imports
All required Python libraries are imported. These include:
- `pandas` and `numpy` for working with structured tabular data.
- `plotly` for creating interactive charts and graphs.
- `jinja2` for loading and rendering the HTML dashboard template.
- `scipy` and `statsmodels` for statistical analysis and hypothesis testing.
- `datetime`, `json`, `os`, and `re` for utility and file handling.

## 2. Configuration
Global variables are defined for input/output file paths, color palettes, and the current report date. These control the behavior and appearance of the dashboard and can be customized if needed.

## 3. Data Loading
Reads in two CSV files:
- `employee_snapshot.csv`: Contains employee ID, job level, role, job function, and manager ID.
- `employee_history.csv`: Contains hire dates and promotion dates.

## 4. Data Cleaning
Dates are parsed and validated. Errors such as invalid or missing promotion dates are handled gracefully. The data is merged on `employee_id` to form a complete record for each person.

## 5. Feature Engineering
New features are calculated:
- Tenure in years
- Time to promotion
- Span of control (number of direct reports per manager)

## 6. Group-Level Metrics
Calculates:
- Average tenure by function and level
- Promotion rates across different roles
- Manager to IC ratios
- Distribution of span of control

## 7. Statistical Testing
Performs:
- T-tests for comparing tenure and span between functions
- Chi-square tests for comparing promotion rates
- Correlation testing for span vs. tenure trends

## 8. Narrative Generation
Builds summary statements that explain the patterns found in the data. Includes p-values and interpretations of significant differences using plain, understandable language.

## 9. Plotly Chart Generation
Charts are created with custom colors, titles, and hover tooltips. Each chart aligns with a specific section in the HTML template.

## 10. HTML Dashboard Rendering
Charts and narratives are injected into a Jinja2 template, then saved as `gem_ip_dashboard.html`. This output can be opened directly in a web browser.

## 11. Output Review
Final checks ensure the output contains all visuals and narratives, matches expected formatting, and renders without error.

