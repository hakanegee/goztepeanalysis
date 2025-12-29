# Exploratory Data Analysis (EDA)

Boxplots are used to visualize differences in player performance distributions across periods.

The EDA reveals:
	•	A shift in the distribution of defensive actions, with lower median values in the post-acquisition period.
	•	Relatively similar distributions for goal contributions per 90, suggesting no major offensive change.
	•	Slight differences in playing time (90s), though with overlapping distributions.

These visual patterns suggest that the most notable change after the Sport Republic acquisition may be defensive rather than offensive.

⸻

# Hypothesis Testing

To formally assess these differences, Welch’s two-sample t-tests are conducted between pre- and post-acquisition periods for each key metric.

# Hypotheses

H₀ (Null Hypothesis):
The Sport Republic acquisition did not lead to meaningful changes in Göztepe’s transfer profiles or the on-field performance of newly transferred players.

H₁ (Alternative Hypothesis):
The Sport Republic acquisition positively influenced Göztepe’s sporting success by introducing a more effective scouting and recruitment strategy, observable through changes in player profiles and on-field performance.

# Results Summary
	•	Defensive actions: A statistically significant difference is observed between periods (p < 0.01).
	•	Playing time (90s): No statistically significant difference detected.
	•	Goal contributions per 90: No statistically significant difference detected.

These results indicate that the primary measurable change following the acquisition is defensive in nature.

⸻

# Interpretation and Link to Sporting Outcomes

The statistically significant reduction in individual defensive actions suggests improved collective organization and positional discipline in the post-Sport Republic period. Rather than relying on frequent individual interventions, the team appears to operate within a more structured defensive system.

Such structural defensive improvements are commonly associated with conceding fewer goals, which in turn contributes to better league results and point accumulation. While this analysis does not directly model league standings, the defensive performance shift provides a plausible mechanism linking recruitment strategy changes to improved sporting outcomes.

⸻

Repository Structure
	•	Analysis(sub2).ipynb: Full EDA and hypothesis testing notebook.
	•	data/fbref/: Cleaned FBref performance datasets used in the analysis.
	•	README.md: This explanatory document.

⸻

# Conclusion

This submission demonstrates how exploratory data analysis and basic hypothesis testing can be used to evaluate organizational change in a football club context. The findings suggest that the Sport Republic acquisition coincides with a defensively oriented performance shift, providing initial quantitative support for changes in recruitment and team structure.

Further analysis in later stages can extend this framework to incorporate league outcomes and additional performance dimensions.
