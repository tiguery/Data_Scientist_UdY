# Developer Salary & Job Satisfaction — Global (Stack Overflow 2024)

**Goal.** Answer five visual questions about global developer **salary** and **job satisfaction**, then fit a tiny model.

## Data (Approved Source)
- **Stack Overflow Developer Survey 2024** → https://survey.stackoverflow.co/
- Download **CSV**: `survey_results_public_2024.csv`
- Place at: `data/survey_results_public_2024.csv`

## Environment
```
pandas
numpy
scikit-learn
matplotlib
seaborn
```

## How to Run
1. Create folders:
   ```
   project/
     data/
     figures/   (optional)
   ```
2. Download the CSV and save as `data/survey_results_public_2024.csv`.
3. Open `developer_survey_notebook.ipynb`, set `CSV_PATH` if needed, and run all cells.
4. The notebook will:
   - Load and lightly clean the data (filter salary to $5k–$500k; drop missing fields).
   - Produce **5 plots** (one per question) using seaborn’s simple style.
   - Train a small **LinearRegression** (optional) and report **R²/MAE**.
   - Run a **scenario**: add **+5 years** to experience and re-predict salary.

## Questions Answered (Each with a Graph)
1) Which countries report the highest average salaries?  
2) Is coding experience related to salary?  
3) How does remote work affect job satisfaction?  
4) Do full-time developers earn more than contractors/self-employed?  
5) Is higher salary linked to higher job satisfaction?  

## Notes
- This is **beginner-friendly**: clear cells, short code, and transparent filters.
- If columns differ slightly, adjust the column name mapping cell near the top.

## License
MIT — adapt freely for coursework.
