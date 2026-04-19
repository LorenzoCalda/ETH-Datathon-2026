# ETH-Datathon-2026

Submission by The Uninformed Priors (Lorenzo Calda, Simone Garuffi, Elijah Tamarchenko, Mateusz Rozalsky) for the UN OCHA **Geo-Insight: Which Crises Are Most Overlooked?** challenge.

## Project Summary

This project builds a data-driven workflow to identify crises where **documented humanitarian need outpaces funding coverage**. Given a country, region, or analytical query, we compute and rank likely overlooked crises using need indicators (for example, people in need and severity context) and financing coverage signals (requirements vs. funding).

The goal is decision support for humanitarian analysts: transparent rankings, map-ready outputs, and short explanations that can be used in briefings.

## What This Repository Contains

- Notebooks in `Code/` for data cleaning, feature construction, exploratory analysis, and crisis ranking logic.
- Raw and intermediate datasets in `Data/`, including HNO/HPC inputs, requirements/funding tables, severity indices, and crisis time series.
- Dashboard artifacts in `Code/Dashboard Databricks/` for communicating results.

## Analytical Approach (Short)

1. Harmonize country/crisis records across HNO/HPC and funding datasets.
2. Apply minimum-need thresholds to keep only materially relevant crises.
3. Compute gap metrics (for example, funding coverage ratio and need-funding mismatch score).
4. Rank crises by overlooked risk and summarize key drivers.
5. Use multi-year signals (where available) to distinguish acute gaps from structural neglect.

## Data Basis

Primary sources follow the challenge guidance and include public OCHA/HDX humanitarian need and funding datasets (HNO/HPC requirements, global requirements and funding, and related reference tables). Any additional enrichment should be explicitly declared in analysis notebooks.

## Expected Outputs

- Ranked list of crises/countries with gap scores.
- Brief rationale for top-ranked overlooked crises.
- Visual outputs suitable for maps or dashboard views.
- Discussion of limitations (missingness, reporting lags, and comparability issues).

## Reproducibility Note

All outputs are grounded in the provided public data. Scores are designed to support analyst judgment, not to automate funding decisions.
