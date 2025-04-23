# Required Python Packages

Below is a list of required Python libraries to successfully run the dashboard notebook.

You can install all of them using the command:

```bash
pip install pandas numpy plotly jinja2 statsmodels scipy
```

## Required Packages and Their Purposes

| Package       | Purpose                                                                 |
|---------------|-------------------------------------------------------------------------|
| pandas        | Data loading, joining, transformation, and export                       |
| numpy         | Numerical calculations for tenure and span metrics                      |
| plotly        | Interactive charting (bar, box, gauge, etc.) with hover and drilldown   |
| jinja2        | Rendering the HTML dashboard from a templated layout                    |
| statsmodels   | Conducting statistical t-tests and regression analysis                  |
| scipy         | Hypothesis testing and statistical summaries                            |

## Recommended Setup

It is advisable to use a virtual environment:

```bash
python -m venv venv
source venv/bin/activate  # or .\venv\Scripts\activate on Windows
pip install -r requirements.txt
```

To lock your environment:

```bash
pip freeze > requirements.txt
```

This ensures that others can replicate your environment with the exact same library versions.
