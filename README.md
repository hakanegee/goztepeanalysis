# Göztepe S.K. Performance Analysis  
### Exploratory Data Analysis, Hypothesis Testing & Machine Learning

---

## 1. Motivation

This project analyzes whether Göztepe S.K.’s squad characteristics and on-field performance changed following the Sport Republic acquisition in 2022.  
The main motivation is to examine if changes in ownership and recruitment strategy are reflected in observable player-level performance indicators, particularly defensive behavior, offensive output, and player usage.

---

## 2. Data Sources

Player-level performance data were collected from **FBref** for selected seasons:

- **Pre-acquisition period:** 2021–2022  
- **Post-acquisition period:** 2024–2025, 2025–2026  

Due to scraping restrictions, all FBref tables were extracted manually and stored as Excel files.

Two types of datasets are used:
- **Standard statistics:** minutes played, goals, assists, goal contributions per 90
- **Miscellaneous statistics:** interceptions, tackles won, fouls, crosses

All raw data files are stored under:
---

## 3. Data Preparation

All datasets were cleaned and merged across seasons.  
Each player-season observation was labeled with:
- `season`
- `period` (Pre-Sport Republic / Post-Sport Republic)

This structure enables direct comparison of player performance before and after the acquisition.

---

## 4. Exploratory Data Analysis (EDA)

Exploratory Data Analysis focuses on visualizing differences in player performance distributions across periods using boxplots.

The following metrics were examined:
- Playing time (90s)
- Goal contributions per 90 minutes
- Defensive actions (interceptions + tackles won)

The EDA shows:
- Similar distributions of goal contributions per 90 across periods, suggesting no major offensive shift.
- Slight differences in playing time with overlapping distributions.
- A clear shift in defensive action distributions after the acquisition.

These visual patterns indicate that post-acquisition changes are more pronounced in defensive behavior rather than offensive output.

---

## 5. Hypothesis Testing

To formally assess observed differences, **Welch’s two-sample t-tests** were conducted between pre- and post-acquisition periods.

### Hypotheses
- **H₀ (Null Hypothesis):** The Sport Republic acquisition did not lead to meaningful changes in player performance.
- **H₁ (Alternative Hypothesis):** The Sport Republic acquisition led to meaningful changes in player performance.

### Results Summary
- No statistically significant difference in goal contributions per 90.
- No statistically significant difference in average playing time.
- A statistically significant difference in defensive actions.

These results support the idea that the acquisition is associated with structural changes in defensive performance.

---

## 6. Machine Learning Application

A supervised machine learning approach was applied to classify whether a player-season observation belongs to the pre- or post-acquisition period.

A **logistic regression** model was implemented using selected performance features.  
The workflow includes:
- Train–test split
- Feature scaling
- Model training and evaluation

Model performance was evaluated using accuracy, F1-score, and classification reports.  
Defensive-related features contributed more strongly to classification performance than offensive metrics, reinforcing findings from EDA and hypothesis testing.

All numerical results and implementation details are provided in the notebook files.

---

## 7. Limitations

- The analysis is limited to selected seasons due to data availability.
- Player-level performance does not fully capture team-level tactical dynamics.
- External factors such as league strength, opponent quality, and coaching changes are not explicitly modeled.

---

## 8. Project Structure

- `data/fbref/` : Raw FBref performance data  
- `submission 2 explanation` : EDA and hypothesis testing analysis  
- `sub3.ipynb` : Machine learning implementation  
- `README.md` : Project overview and summary  

---

## 9. Conclusion

The analysis suggests that the Sport Republic acquisition did not immediately increase offensive output but coincided with measurable changes in defensive behavior. These defensive adjustments may contribute indirectly to improved league performance over time.

Detailed numerical results and code are intentionally kept within notebooks, while this README provides a structured summary of motivation, methods, findings, and limitations.
