Netflix Analysis

📊 A Python-based Exploration of Netflix Viewing History

This repository contains a Jupyter Notebook that performs exploratory data analysis (EDA) on Netflix viewing history using Python libraries like pandas, matplotlib, and seaborn. The goal is to understand and visualize trends in Netflix streaming activity such as what content was watched, durations, patterns over time, device types, and content categories.  ￼

⸻

📁 Repository Structure

.
├── Netflix_Analysis.ipynb       # Main analysis notebook
├── data/                        # (Optional) raw and processed datasets
├── viz/                         # Exported visualization images & results
├── requirements.txt             # Libraries & dependencies
├── LICENSE                      # License information (optional)
└── README.md                   # Project documentation (this file)


⸻

🧠 Project Overview

Netflix tracks a user’s complete viewing history in CSV files. In this project, we:
	1.	Load and inspect the Netflix viewing history dataset
	2.	Clean and preprocess the data
	3.	Extract useful features like watch times, dates, content types
	4.	Perform analysis and data visualizations
	5.	Generate insights about viewing habits and patterns

This notebook is structured so that you can follow each step interactively or reproduce the analysis yourself.  ￼

⸻

🚀 Getting Started

🔧 Prerequisites

Install Python and set up a virtual environment (optional but recommended).

# Create and activate a venv (optional)
python -m venv venv
source venv/bin/activate     # On Windows use: venv\Scripts\activate

📦 Install Dependencies

Install required libraries:

pip install -r requirements.txt

Or individually:

pip install pandas matplotlib seaborn jupyterlab


⸻

📊 How It Works

🗃️ 1. Loading Data
	•	Load your Netflix viewing history CSV file (e.g., ViewingActivity.csv)
	•	Use pandas to read and inspect the table structure

🧹 2. Cleaning the Data
	•	Convert date/time strings to datetime types
	•	Remove unneeded columns (e.g., bookmarks, attributes)
	•	Clean entries and filter out irrelevant content

📆 3. Feature Extraction

Generate new columns such as:
	•	Watch date and time
	•	Content type (movie vs. TV show)
	•	Duration in minutes
	•	Day of week, month, and year derived from timestamps

📈 4. Analysis & Visualization

Using matplotlib and seaborn:
	•	Bar charts showing watch counts by genre or day
	•	Line plots of viewing activity over time
	•	Histograms of session durations
	•	Device type breakdowns

Visual charts help uncover viewing trends and patterns.

⸻

📝 Example Code Snippet

Here’s an example of how data loading and preprocessing might look:

import pandas as pd

# Load viewing history
df = pd.read_csv('ViewingActivity.csv')

# Convert start time to datetime
df['Start Time'] = pd.to_datetime(df['Start Time'])

# Extract components
df['Year']  = df['Start Time'].dt.year
df['Month'] = df['Start Time'].dt.month_name()

(This structure can be found directly in the Jupyter Notebook cells.)  ￼

⸻

📌 Key Findings (Example)

After cleaning and analyzing the data:
	•	Most watched days and months
	•	Popular content based on frequency
	•	Viewing trends over the course of the year
	•	Patterns by device type and session length

*Actual findings depend on your dataset — the notebook includes charts and tables.  ￼

⸻

🧩 Contributing

Contributions are welcome! You can:
	•	Add more visualization types
	•	Include statistical summaries
	•	Integrate time-series forecasting
	•	Build dashboards (e.g., using Plotly or Dash)

⸻

🎓 License

Licensed under the MIT License. Feel free to use or extend this project.

⸻

📫 Questions

Have questions or want help extending this? Just ask!

Happy analyzing 🎉
