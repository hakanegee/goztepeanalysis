# Project Proposal: Göztepe’s Scouting Strategy and Sporting Recovery
# Motivation

Since my childhood, I have always been passionate about football — both playing and watching it. In recent months, I have started merging this long-term interest with my academic and professional life. I have taken courses on scouting, conducted independent research, connected with professionals on LinkedIn, and begun shaping a career path specifically focused on football analytics and recruitment.

I chose Göztepe as the focus of this project because they are one of the few clubs in Turkey that operate with a systematic, data-driven approach and make strategically sound sporting decisions. This makes the project particularly meaningful for me, as I have actively been networking with professionals in the football industry and was fortunate to connect with Rasmus Ankersen, the president of Göztepe and co-founder of Sport Republic, which owns multiple football clubs across Europe. I closely follow their innovative and analytical approach to football management and scouting.

Beyond my personal interest, this project is also relevant from a broader football analytics perspective. Göztepe stands out as a rare example in Turkish football where modern scouting principles — such as targeting young players with high potential, system-compatible profiles, and undervalued talents from less prominent leagues — have been applied consistently. Instead of relying primarily on established players, the club appears to have shifted toward a long-term recruitment vision focused on sustainability and development.

Lastly, on a personal note, I aspire to work or intern in a football club in the near future. I have already applied to PLAIER, an AI- and data-driven scouting platform, as part of this goal. This project directly reflects my professional ambitions and provides an opportunity to apply data science tools to a real-world football problem. My main motivation for taking this course was to develop a project centered on scouting strategies, and choosing Göztepe allows me to produce work that is valuable both academically and professionally.


# Project Objective and Research Question

The objective of this project is to examine whether the acquisition of Göztepe by Sport Republic in 2022 coincided with a structural change in the club’s scouting and transfer strategy, and whether this change aligns with the club’s subsequent sporting recovery.

Research Question:
Did Göztepe’s transfer and scouting strategy change after the Sport Republic acquisition in 2022, and can this change be observed through differences in transfer profiles and basic player performance indicators?


# Data Sources

# Transfer Data (Primary Dataset)

The primary dataset will be collected from Transfermarkt, a publicly available football transfer database.

Season-level transfer data for Göztepe will be collected for the following seasons:
	•	2020–2021
	•	2021–2022
	•	2022–2023
	•	2023–2024
	•	2024–2025
	•	2025–2026

Each season has a dedicated Transfermarkt page listing all incoming and outgoing transfers.

The following variables will be collected:
	•	Player name
	•	Age at time of transfer
	•	Position
	•	Transfer fee
	•	Origin club (for incoming transfers)
	•	Destination club (for outgoing transfers)
	•	Season

The data will be collected programmatically using Python libraries such as requests, pandas, and BeautifulSoup, by parsing HTML tables and converting them into structured DataFrames.


# Performance Data (Enrichment Dataset)

To enrich the transfer data with on-field performance indicators, publicly available player statistics from FBref will be used for seasons in which Göztepe competed in the Süper Lig.

Due to access restrictions on automated scraping from FBref, relevant performance tables (including standard and miscellaneous statistics such as minutes played, goals, assists, and selected defensive or involvement metrics) will be manually extracted and stored in structured Excel files. These Excel files will later be imported into Python and merged with the transfer dataset using player names and seasons as keys.

This enrichment step allows the project to connect recruitment decisions with basic on-field performance outcomes.


# Planned Data Collection and Preparation

The planned data preparation steps include:
	•	Cleaning and standardizing player names across datasets
	•	Converting transfer fees into numeric format
	•	Handling missing or incomplete records
	•	Structuring the data to allow season-level and period-level comparisons

Incoming transfers will be the primary focus of the analysis, as they directly reflect the club’s scouting and recruitment strategy.

### Performance Data (FBref)

Player-level performance statistics (standard and miscellaneous stats) were obtained from FBref for selected Süper Lig seasons. Due to FBref’s automated scraping restrictions, these tables were manually extracted and stored as structured Excel files under `data/fbref/`. These datasets are used to evaluate the on-field contribution of newly transferred players before and after the Sport Republic acquisition.


# Planned Analysis

The analysis will proceed in the following stages:
	1.	Descriptive analysis of transfer characteristics (e.g., age distributions, transfer volume by season).
	2.	Exploratory comparisons between two periods:
	•	Pre-Sport Republic: 2020–2021 and 2021–2022
	•	Post-Sport Republic: 2022–2023 to 2025–2026
	3.	Linking newly transferred players to basic performance indicators to explore their potential contribution to sporting outcomes.


# Planned Exploratory Data Analysis (EDA)

The planned EDA will include:
	•	Summary statistics of incoming transfers (average age, number of arrivals per season).
	•	Visualization of age distributions to examine shifts in recruitment profiles.
	•	Season-level comparison of transfer activity to identify changes in recruitment intensity.
	•	Integration of basic performance metrics to contextualize transfer decisions.

At the proposal stage, these analyses are planned but not yet executed.


# Hypothesis and Planned Statistical Tests

The central hypothesis of this project is that the acquisition of Göztepe by Sport Republic in 2022 positively affected the club’s sporting success through changes in its scouting and recruitment strategy.

H₀ (Null Hypothesis):
The Sport Republic acquisition did not lead to meaningful changes in Göztepe’s transfer profiles or the on-field performance of newly transferred players.

H₁ (Alternative Hypothesis):
The Sport Republic acquisition positively influenced Göztepe’s sporting success by introducing a more effective scouting and recruitment strategy, observable through changes in incoming player profiles and their subsequent on-field performance.

To evaluate this hypothesis, the project plans to use:
	•	Period-based comparisons between pre- and post-2022 transfer characteristics.
	•	Basic statistical tests (such as two-sample t-tests where appropriate) to compare player profiles across periods.

Formal hypothesis testing and interpretation will be conducted in later stages of the project.


# Expected Contribution

This project aims to provide a structured, data-driven case study on how changes in scouting and recruitment strategy may be associated with sporting recovery, using Göztepe as a real-world example.
