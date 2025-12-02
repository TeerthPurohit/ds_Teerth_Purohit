README.md
📊 Data Science Submission — Trader Behavioral Analysis
Author: Teerth Purohit
Date: December 2025
________________________________________
📁 Project Overview
This project investigates the relationship between market sentiment (Fear vs. Greed) and trading performance using real historical trade data and a Bitcoin sentiment index. The objective is to identify patterns in profitability, capital efficiency, trade timing, and directional edge (long vs short).
The analysis is implemented in Python using a Jupyter/Colab notebook, with reproducibility and data transparency in mind.
________________________________________
📂 Folder Structure
ds_Teerth_Purohit/
├── notebook_1.ipynb            # Main analysis notebook
├── ds_report.pdf               # Final PDF report (6+ pages)
├── README.md                   # Project description and instructions
│
├── csv_files/                  # Input & processed data
│   ├── historical_data.csv     # Raw trade data
│   ├── fear_greed_index.csv    # Sentiment dataset
│   ├── advanced_analysis_by_mood.csv
│   ├── day_of_week_volume.csv
│   ├── hourly_winrate.csv
│   ├── side_performance.csv
│   ├── top10_coin_pnl.csv
│
└── outputs/                    # Generated visualizations
    ├── pnl_vs_mood.png
    ├── strategy_dashboard.png
    ├── time_analysis.png
    └── psychology_check.png
________________________________________
⚙️ Setup Instructions
This notebook is designed to run without any external downloads, cloud connections, or Drive mounting.
All paths are relative to the project root.
Requirements
•	Python 3.10+
•	pandas
•	matplotlib
•	seaborn
Installation (optional)
pip install pandas matplotlib seaborn
________________________________________
▶️ Running the Notebook
1.	Open notebook_1.ipynb in Jupyter Notebook, Jupyter Lab, or Google Colab.
2.	Ensure the current working directory is set using:
import os
os.chdir('/content/drive/MyDrive/Colab Notebooks/ds_Teerth_Purohit')
⚠️ If running locally:
You do not need to change directories as long as the folder structure remains the same.
3.	Run the notebook cells from top to bottom.
Summary tables will automatically be saved to /csv_files/ and charts saved to /outputs/.
________________________________________
📑 Data Sources & Notes
•	historical_data.csv contains trade-level execution data:
timestamp, direction (BUY/SELL), instrument, size (USD), fees, and realized PnL.
•	fear_greed_index.csv contains daily sentiment classification values:
Extreme Fear, Fear, Neutral, Greed, Extreme Greed.
•	Date alignment is performed using trade_date = date(timestamp).
This creates a clean one-to-many merge between sentiment and trade tables.
•	ROI is defined as:
ROI (%) = (Closed PnL / Position Size USD) * 100
________________________________________
📌 Outputs & Interpretation
The notebook produces:
•	pnl_vs_mood.png — average profit by sentiment
•	strategy_dashboard.png — ROI, Win Rate, Buy Ratio & Avg Trade Size by sentiment
•	time_analysis.png — volume and win rate by day & hour
•	psychology_check.png — long vs short performance & top assets
These visualizations are referenced throughout ds_report.pdf.
________________________________________
🔍 Reproducibility Checklist
✔️ No absolute file paths
✔️ All input files stored locally in csv_files/
✔️ All outputs saved to versioned folder outputs/
✔️ Processed summary tables saved as CSV for transparency
✔️ All analysis steps documented in commented notebook cells
________________________________________
✔️ Status
Complete and ready for evaluation.
If you encounter any issues running the notebook, please confirm that all filenames are spelled exactly as shown in the folder structure.
________________________________________
