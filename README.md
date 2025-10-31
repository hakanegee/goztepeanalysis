# Göztepe’s scouting achievements and their success in executing financially and sportingly effective transfers.

# Motivation: Why will I work on this project?

Since my childhood, I have always been passionate about football — both playing and watching it. In recent months, I’ve started merging this passion with my academic and professional life. I’ve taken courses on scouting, conducted research, connected with professionals on LinkedIn, and begun shaping a career path in this specific area of football.

I chose Göztepe as the focus of my project because they are one of the few clubs in Turkey that operate with a systematic, data-driven approach and make impressive business and sporting decisions. This makes the project even more exciting for me, as I have been networking with professionals in the football industry and was fortunate to connect with Rasmus Ankersen, the president of Göztepe and co-founder of Sport Republic, which owns multiple clubs across Europe. I closely follow their innovative and analytical methods of football management.

Beyond my personal interest, this project is also meaningful from a broader perspective. Göztepe stands out as one of the rare Turkish clubs that apply modern scouting strategies similar to world-class European teams. Instead of focusing solely on established players, they strategically sign young talents with high potential, system-fitting players, and underrated names from less-known leagues — showcasing a forward-thinking approach in Turkish football.

Lastly, on a personal note, I aspire to work or intern in a football club in the near future. I have already applied to PLAIER, an AI- and data-driven scouting platform, as part of this goal. I’m genuinely excited about this project because it reflects my professional ambitions and directly supports my career applications. My main motivation for taking this course was to create a project on scouting strategies, and choosing Göztepe allows me to develop something valuable both academically and professionally.

The hypothesis tested in this project will be that the acquisition of Göztepe by Sport Republic in 2022 led to a measurable improvement in the club’s transfer strategy and overall performance compared to the pre-acquisition period (2020–2022).

# Data Source 

The primary dataset for this project will be collected from Transfermarkt, a publicly available and reputable football database that provides detailed transfer information for professional clubs.

I plan to collect data from Göztepe’s transfer history between 2020 and 2025, focusing on both incoming and outgoing players. This time frame is strategically selected to compare the pre- and post-Sport Republic eras, as in August 2022, Göztepe sold 70% of its shares to Sport Republic. My aim is to demonstrate that this partnership marked a turning point in the club’s transfer and scouting strategy. Therefore, analyzing the two distinct periods — before (2020–2022) and after (2022–2025) the Sport Republic acquisition — will help reveal how Göztepe’s transfer behavior, player profiles, and performance outcomes have evolved over time.

The dataset will be extracted directly from Transfermarkt’s official pages using Python libraries such as pandas, requests, and BeautifulSoup. The website presents transfer information in HTML tables, which can be read and transformed into structured DataFrames. Each row in the dataset will represent one player transfer, and the key variables to be collected are:
	•	Player Name
	•	Age (at time of transfer)
	•	Position
	•	Nationality
	•	Transfer Fee (€)
	•	Previous Club (for incoming transfers)
	•	New Club (for outgoing transfers)
	•	Season / Transfer Window (Summer or Winter)

After collection, the data will be cleaned and preprocessed (handling missing values, converting currencies to numeric format, and standardizing categorical labels). This structured dataset will allow for year-over-year comparisons, positional distributions, and correlation analysis between variables such as transfer fee, age, and performance metrics.

This enriched dataset will enable a deeper analysis of transfer efficiency, such as examining whether younger, lower-cost players acquired after the Sport Republic partnership have produced better on-field performance compared to earlier, more experienced signings.

All collected data will be used for descriptive and comparative analysis (e.g., averages, distributions, and trends), followed by machine learning applications such as:
	•	Regression models to study how player attributes and transfer fees relate to performance outcomes, and
	•	Clustering analysis to group players or transfer types based on similar characteristics (e.g., “young talents,” “experienced leaders,” “budget signings”).

Ultimately, this structured dataset will allow for a clear, data-driven exploration of how Göztepe’s scouting and transfer strategy evolved between 2020 and 2025, especially under the data-oriented management of Sport Republic.
