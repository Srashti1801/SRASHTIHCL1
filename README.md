# Employee Attrition Analysis (Sample Data Analyst Project)

A beginner-friendly data analysis project for B.Tech 1st Year – Data Analyst learners.

This project analyses employee attrition risk using Python, pandas, NumPy and matplotlib. It explores how factors such as working hours, salary, department, city, work mode and job level are associated with the risk score.

The dataset is synthetic (AI-generated). It contains no real employee personal data.

## Business problem

The HR team of a mid-sized Indian IT and services company wants to understand which employee groups may be more likely to leave. Replacing employees can be costly, so HR needs evidence-based insights to identify patterns and prioritise retention support.

This project treats `Attrition_Risk_Score` as an existing descriptive score from 0 to 100. A higher score indicates a higher level of attrition risk. The project is exploratory analysis; it does not predict future resignations.

## Questions answered

- What does the overall distribution of employee attrition risk scores look like?
- How are average weekly working hours and monthly salary associated with attrition risk?
- Does the average risk score differ by department, city, work mode or job level?
- Which employees are classified as high risk (risk score of 70 or above), and what common characteristics do they have?

## Dataset

`data/raw/attrition_data.csv` – 255 raw rows and 12 columns.

The dataset contains the following fields:

`Employee_ID`, `Department`, `City`, `Work_Mode`, `Job_Level`, `Age`, `Years_At_Company`, `Monthly_Salary_INR`, `Avg_Weekly_Hours`, `Commute_Distance_Km`, `Last_Appraisal_Date`, `Attrition_Risk_Score`.

The raw file intentionally includes data-quality issues such as missing values, duplicate records, inconsistent category text and invalid age values so that data cleaning can be practised.

After cleaning, the dataset contains **250 rows**.

## Project structure

```text
employee-attrition-analysis/
├── data/
│   ├── raw/
│   │   └── attrition_data.csv
│   └── processed/
│       └── attrition_data_clean.csv
├── notebooks/
│   └── employee_attrition_analysis.ipynb
├── images/                         (charts saved by the notebook)
├── documents/                      (project documentation)
└── README.md
```

*Note: Update notebook and image filenames in this section if the names in your GitHub repository are different.*

## How to run

The analysis was developed using Google Colab.

1. Open [Google Colab](https://colab.research.google.com/).
2. Open or upload the analysis notebook from the `notebooks/` folder.
3. Upload the dataset or make sure the notebook can access `data/raw/attrition_data.csv`.
4. Run the notebook cells from top to bottom.

To run the project locally instead, clone the repository and install the required libraries:

```bash
git clone https://github.com/Srashti1801/SRASHTIHCL1.git
cd SRASHTIHCL1
pip install pandas numpy matplotlib
```

Then open the notebook using Jupyter:

```bash
jupyter notebook
```

## Steps followed

1. **Load and inspect data** – read the CSV file and check its shape, columns, data types, missing values and duplicate records.
2. **Clean data** – remove duplicates, handle missing values, standardise city labels and correct invalid age values.
3. **Create new columns** – derive fields such as `Annual_Salary`, `Risk_Category` and `Experience_Group`.
4. **Exploratory data analysis** – calculate descriptive statistics, compare groups and study relationships using charts and correlations.
5. **Insights and recommendations** – summarise the patterns and suggest areas where HR may review employee support and retention practices.

## Key findings

The reported findings from the cleaned dataset include:

- The average attrition risk score is approximately **50.51**.
- **15 out of 250 employees (6%)** have a high-risk score of **70 or above**.
- Average weekly working hours have a positive association with the risk score (reported correlation approximately **+0.57**).
- Monthly salary has a negative association with the risk score (reported correlation approximately **−0.57**).

These findings describe the synthetic dataset only. Correlation does not prove that working hours or salary cause employees to leave.

## Charts

The project analysis and presentation cover the following visualisations:

- **Overall risk:** distribution of attrition risk scores.
- **Working hours:** relationship between average weekly hours and risk score.
- **Salary:** relationship between monthly salary and risk score.
- **Employee groups:** comparisons across department, city, work mode and job level.
- **Risk categories:** overview of risk bands and the high-risk employee group.

If chart images are saved in the `images/` directory, they can be displayed here. Replace the example filenames with the actual image names in the repository.

```markdown
![Overall attrition risk distribution](images/risk_distribution.png)
![Weekly hours and attrition risk](images/weekly_hours_vs_risk.png)
![Monthly salary and attrition risk](images/salary_vs_risk.png)
```

## Tools

- Python
- pandas
- NumPy
- matplotlib
- Google Colab
- Git and GitHub

The Python and library versions were not recorded.

## Recommendations

Based on the patterns observed, HR teams could:

- Review workload and working-hour patterns in groups with higher risk scores.
- Arrange regular check-ins with employees in higher-risk groups.
- Review compensation patterns in the context of role, experience and responsibilities.
- Use the analysis as an initial guide for further investigation, not as the only basis for employment decisions.

## Limitations

- The dataset is synthetic and may not reflect real employee behaviour.
- The analysis uses 250 cleaned records, so findings should be interpreted cautiously.
- The risk score is already present in the dataset; this project does not build or validate a machine-learning prediction model.
- The results show associations, not cause-and-effect relationships.

## Author

**Srashti Gupta**  
B.Tech 1st Year – CSE-13  
ABES Engineering College  
GitHub: [Srashti1801/SRASHTIHCL1](https://github.com/Srashti1801/SRASHTIHCL1)

---

*Created as part of a beginner-level Data Analyst training project.*
