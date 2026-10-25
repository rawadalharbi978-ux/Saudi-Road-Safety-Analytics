# Saudi Road Safety Analytics | 2023–2024

A reproducible **descriptive data analysis** of national road safety indicators and the distribution of serious road traffic accidents across Saudi Arabia's 13 administrative regions.

## Questions

- How did reported serious accidents, fatalities, and injuries change between 2023 and 2024?
- Which regions accounted for the largest numbers of serious accidents in 2024?
- How were accidents distributed within and outside cities?

## Source and verification

**Official source:** General Authority for Statistics (GASTAT), *Road Transport Statistics 2024* — https://www.stats.gov.sa/en

The analysis uses a fixed snapshot of annual and regional data reconstructed from the earlier project notebook. The snapshot was **checked against the official Arabic Excel workbook** (`Road Transport Statistics 2024_AR (1).xlsx`). The checks found:

- **39/39 exact matches** across the 13 regions for within-city, outside-city, and total serious accident counts (sheet `5-5`).
- Matching annual serious accident totals for 2023 and 2024 (sheet `5-3`).
- Matching 2024 national fatalities and injuries (sheet `5-1`).

The complete ZIP includes the original Excel workbook and `Saudi_Road_Safety_Official_Regional_Audit.csv` as an audit trail. The notebook also contains a verification cell that reruns the comparison if the workbook is in the working directory. The main analysis does not require an online download.

## Methods

- Data integrity and arithmetic consistency checks
- National absolute and percentage changes (2023–2024)
- Reported fatalities and injuries per 100 serious accidents (descriptive ratios, not individual crash probabilities)
- Regional counts, national shares, and within-/outside-city distributions
- Tables, visualizations, and CSV exports

**Tools:** Python, pandas, NumPy, matplotlib, seaborn. No machine learning is used or needed for the research questions.

## Key findings

- Serious accidents increased from **16,534** (2023) to **17,231** (2024), approximately **4.22%**.
- Fatalities decreased from **4,423** to **4,282**, approximately **3.19%**.
- Injuries increased from **24,002** to **24,077**, approximately **0.31%**.
- In 2024, **10,392** serious accidents were recorded within cities and **6,839** outside cities.
- **Makkah** had the highest reported count: **5,825**, or approximately **33.81%** of the national total.

These are **reported counts**, not measures of individual or regional accident risk.

## Reproduce the analysis

1. Open `Saudi_Road_Safety_Analytics_Polished_FINAL.ipynb` in Google Colab or Jupyter.
2. Run all cells. The main analysis uses the embedded, verified snapshot.
3. To rerun the independent official-source audit, put `Road Transport Statistics 2024_AR (1).xlsx` in the notebook's current working directory before running Section 8.
4.⁠ ⁠Generated charts and CSV files are included in the repository root. Running the notebook also saves new outputs to road_safety_outputs/.
## Package contents

- `Saudi_Road_Safety_Analytics_Polished_FINAL.ipynb` — notebook with code and saved outputs
- `README.md` — project description and methods
- Saudi_Road_Safety_Academic_Report.pdf — academic project report.
- - `Road Transport Statistics 2024_AR (1).xlsx` — original official source workbook
- `Saudi_Road_Safety_Official_Regional_Audit.csv` — regional comparison record
  
- Four PNG figures and three exported CSV files — saved in the repository root directory.
## Limitations

The national comparison covers two years only. Aggregated accident counts cannot establish causality or relative regional risk without exposure measures such as population, traffic volume, or vehicle distance traveled. The project is descriptive and makes no predictive claims.
