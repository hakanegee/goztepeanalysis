# Göztepe S.K. Performance Analysis  
### Exploratory Data Analysis, Hypothesis Testing & Machine Learning

---

## 1. Motivation

This project examines whether Göztepe S.K.’s sporting profile and on-field performance changed following the Sport Republic acquisition in 2022.  
The core motivation is to understand whether ownership change and the associated recruitment strategy are reflected both in **transfer behavior** and **player-level match performance**.

By combining transfer market data with on-field statistics, the project aims to connect squad construction decisions with observable performance outcomes.

---

## 2. Data Sources

Two complementary data sources are used:

### Transfermarkt (2020–2026)
- Player transfer histories
- Age profiles
- Transfer fees and squad composition indicators

Transfermarkt data is used to characterize **recruitment strategy changes** before and after the acquisition.

### FBref (Selected Seasons)
- Player-level match performance statistics
- Minutes played, goals, assists, defensive actions, and related metrics

FBref data is used to evaluate **on-field performance outcomes** associated with those recruitment decisions.

All datasets were manually collected and stored locally due to scraping restrictions.

---

## 3. Data Preparation

All datasets were cleaned and standardized across seasons.

Key preprocessing steps include:
- Season labeling
- Creation of a binary period indicator:
  - **Pre-Sport Republic** (2021–2022)
  - **Post-Sport Republic** (2024–2025, 2025–2026)
- Merging player-level observations across seasons

Transfermarkt and FBref datasets are analyzed jointly at the conceptual level, while remaining separate at the data level due to differing granularities.

---

## 4. Exploratory Data Analysis (EDA)

EDA focuses on identifying distributional changes in player performance after the acquisition.

Boxplots are used to visualize differences across periods for:
- Playing time (90s)
- Goal contributions per 90 minutes
- Defensive actions (interceptions + tackles won)

Key observations:
- Goal contribution distributions remain largely similar across periods, suggesting no immediate offensive shift.
- Playing time shows moderate variation but with overlapping distributions.
- Defensive action distributions change noticeably in the post-acquisition period.

These patterns suggest that post-acquisition changes are more defensive and structural rather than offensive.

---

## 5. Hypothesis Testing

To formally assess observed differences, **Welch’s two-sample t-tests** are conducted between pre- and post-acquisition periods.

### Hypotheses
- **H₀ (Null Hypothesis):** The Sport Republic acquisition did not lead to meaningful changes in player performance.
- **H₁ (Alternative Hypothesis):** The Sport Republic acquisition led to meaningful changes in player performance.

### Results Summary
- No statistically significant change in goal contributions per 90.
- No statistically significant change in average playing time.
- A statistically significant change in defensive actions.

These results support the interpretation that the acquisition coincides with a defensive reorientation rather than immediate offensive gains.

---

## 6. Machine Learning Application

A supervised machine learning approach is applied to classify whether a player-season observation belongs to the pre- or post-acquisition period.

A **logistic regression** model is implemented using performance-related features derived from FBref data.

The workflow includes:
- Feature selection
- Train–test split
- Feature scaling
- Model training and evaluation

Model performance is evaluated using accuracy, F1-score, and classification reports.  
Defensive performance variables show stronger predictive power, aligning with EDA and hypothesis testing results.

All numerical outputs and implementation details are provided in the notebook files.

---

## 7. Limitations

- Transfermarkt and FBref data operate at different granularities and cannot be merged player-by-player for all observations.
- The number of seasons analyzed is limited by data availability.
- Team-level tactical factors and opponent strength are not explicitly modeled.

---

## 8. Project Structure

- `data/` : Transfermarkt and FBref datasets  
- `submission 2 explanation` : EDA and hypothesis testing  
- `sub3.ipynb` : Machine learning implementation  
- `README.md` : Project overview and summary  

---

## 9. Conclusion

By jointly analyzing Transfermarkt recruitment data and FBref performance statistics, the project shows that the Sport Republic acquisition is associated with a measurable shift toward defensive performance characteristics rather than immediate offensive improvement.

The findings suggest that changes in squad construction strategy may first manifest through defensive stability, which can indirectly contribute to improved league outcomes over time.
