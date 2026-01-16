# Project Success Analytics Case Study

Where are resources overallocated?

**Stakeholder:** Resource Manager

## Key Insights

- Bench time under 4 hours/week signals overallocation risk.
- Billable hours above 42/week precedes overallocation flags.
- FTE above 1.2 on a single initiative raises overload probability.

## Dataset

Primary file: `data/resource_utilization.csv`  
Target variable: `overallocated`

## Getting Started

```bash
pip install -r requirements.txt
jupyter notebook notebooks/01_exploration.ipynb
```


## Next Steps

**Done.** Class-weight tuning and SHAP explainability are implemented — see ### Implemented below.

---
*Analytics portfolio project — 2025-09*

### Implemented

```bash
pip install -r requirements.txt
python src/train.py && python src/explain.py
```