# Project Success Analytics

## Overview

This repository contains a **portfolio-ready analytics project** designed for aspiring Business Analysts, Program Managers, and Data Analysts who want to showcase their data-driven skills on GitHub. It demonstrates end‑to‑end workflow for working with a synthetic dataset that simulates real‑world project performance metrics. The project includes data generation, exploratory data analysis (EDA), feature engineering, classification and regression modeling, and clear documentation.

The core idea is to predict whether a project will succeed (binary classification) and to forecast the project’s success score (regression) using features such as team size, budget, risk level, complexity, scope changes, and satisfaction ratings. All data is **synthetically generated**—there is no personally identifiable or proprietary information included.

## Repository Structure

```text
business_analytics_project/
├── data/
│   └── synthetic_project_data.csv      # Generated dataset with 500 projects
├── notebooks/
│   └── project_success_analysis.ipynb  # Executed analysis notebook with EDA & models
├── requirements.txt                    # Python dependencies
└── README.md                           # Project documentation and instructions
```

## Dataset

The `synthetic_project_data.csv` file contains 500 records, each representing a distinct project. Important columns include:

| Column | Description |
|------|-------------|
| `project_id` | Unique identifier for each project |
| `start_date` | Random start date between 2020‑01‑01 and 2023‑12‑31 |
| `end_date` | Calculated end date based on actual duration |
| `planned_duration_days` | Intended project duration (in days) |
| `actual_duration_days` | Actual project duration (in days) |
| `team_size` | Number of team members (5–30) |
| `budget` | Planned project budget (USD) |
| `actual_spent` | Actual spend based on budget and budget overrun |
| `risk_level` | Risk level on a 1–5 scale |
| `complexity` | Project complexity: Low, Medium, or High |
| `domain` | Project domain: IT, Finance, Marketing, Operations, HR, or R&D |
| `scope_changes` | Number of scope changes requested |
| `satisfaction_rating` | Stakeholder satisfaction on a 1–5 scale |
| `budget_overrun_percentage` | Percent overspend (negative values indicate underspend) |
| `success_metric` | Synthesised continuous success score (0–100) |
| `success` | Binary label indicating whether the success metric exceeded 60 |

These features were generated using reasonable assumptions: higher risk and complexity penalize success, while higher satisfaction scores help it. Delays, scope changes, and budget overruns also negatively impact the success metric. Full details of the generation process can be found in the `notebooks/project_success_analysis.ipynb` notebook.

## Getting Started

### Prerequisites

- Python 3.8 or later
- Jupyter Notebook or JupyterLab (for interactive exploration)

### Setup

1. **Clone the repository** (after this repository is available on GitHub):

   ```bash
   git clone https://github.com/<your-username>/business_analytics_project.git
   cd business_analytics_project
   ```

2. **Create a virtual environment** (optional but recommended) and activate it:

   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
   ```

3. **Install dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter Notebook**:

   ```bash
   jupyter notebook notebooks/project_success_analysis.ipynb
   ```

   The notebook is fully executed with output cells. You can rerun the notebook or modify it to experiment with the models and visualizations.

## Usage

- **Data Exploration**: Use the notebook to explore distributions, correlations, and relationships between variables. Customize the EDA section to add more plots or statistical tests.
- **Modeling**: Experiment with different algorithms, adjust hyperparameters, or perform cross‑validation to improve predictive performance.
- **Feature Engineering**: Try creating new features—for example, ratios between budget and team size—or incorporate time‑based features like quarter or year extracted from the start date.
- **Extensibility**: The synthetic dataset can be regenerated or extended by modifying the data generation script (not included in the repository). Feel free to adapt the dataset to reflect industry‑specific metrics relevant to your background.

## License

This project is released under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

This repository and notebook were created using a generative AI assistant. All data is synthetic and intended solely for demonstration and educational purposes.
