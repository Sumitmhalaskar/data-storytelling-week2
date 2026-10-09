# Telling the Story of Global Cyber Threats

Week 2 task: advanced data visualization and storytelling with Python.
This project turns a table of 3,000 cyber incidents (2015 to 2024) into a short data story for a non-technical audience, using Matplotlib, Seaborn and Plotly.

## Story question

> Which cyber attacks cost the most, who gets hit hardest, and does the choice of defense tool actually help organizations recover faster?

## Dataset

- **Name:** Global Cybersecurity Threats (public dataset, Kaggle)
- **Size:** 3,000 incidents, 10 columns, no missing values
- **Period:** 2015 to 2024
- **Columns:** country, year, attack type, target industry, financial loss (million $), number of affected users, attack source, security vulnerability type, defense mechanism used, incident resolution time (hours)

## Key findings

- Cyber attacks caused about **151.5 billion dollars** in losses. After a dip in 2019, yearly losses settled at a higher level of roughly 15 to 16 billion dollars.
- **DDoS** (27,631 million $) and **Phishing** (26,693 million $) cause the most total damage, but the gaps between attack types are modest.
- **IT** (24,810 million $) and **Banking** (22,772 million $) are the hardest-hit industries. The biggest single hotspot is **Phishing on Banking** (5,146 million $).
- The **UK**, **Germany** and **Brazil** lose the most. China loses the least.
- **No defense tool clearly speeds up recovery.** Median resolution times differ by only 3.5 hours (Firewall 34 h, VPN 37.5 h).
- **Breach size does not predict cost.** The correlation between users affected and financial loss is 0.002.

## Figures

| # | Figure | Chart type | Library |
|---|--------|-----------|---------|
| 1 | Attacks and losses over time | Line charts | Matplotlib |
| 2 | Total loss by attack type | Ranked horizontal bars | Matplotlib |
| 3 | Industry x attack type | Heatmap | Seaborn |
| 4 | Total loss by country | Map (choropleth, interactive) | Plotly |
| 5 | Resolution time by defense | Box plot | Seaborn |
| 6 | Users affected vs. financial loss | Scatter plot (interactive) | Plotly |

![Figure 1](fig1_trend.png)
![Figure 2](fig2_attack_type.png)
![Figure 3](fig3_heatmap.png)
![Figure 4](fig4_map.png)
![Figure 5](fig5_defense_box.png)
![Figure 6](fig6_scatter.png)

## Interactive charts

Figures 4 and 6 are interactive Plotly charts (hover for exact values). GitHub only shows the HTML code, so **download `fig4_map.html` and `fig6_scatter.html` and open them in a web browser**.

## Repository contents

| File | Description |
|------|-------------|
| `Cyber_Data_Storytelling_Report.docx` | Final report: introduction, methods, visual analyses, implications, conclusion |
| `week2_clean.ipynb` | Clean Jupyter notebook with all the code |
| `week2_cyber_storytelling.py` | The same code as a single Python script |
| `Global_cyber_tread.csv` | Original dataset |
| `cleaned_cyber.csv` | Cleaned data saved by the code |
| `fig1_trend.png` ... `fig6_scatter.png` | The six figures (300 dpi) |
| `fig4_map.html`, `fig6_scatter.html` | Interactive versions of Figures 4 and 6 |

## How to run

1. Install the libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn plotly
   ```
   Optional, to export Plotly charts as PNG files: `pip install kaleido`
2. Keep `Global_cyber_tread.csv` in the same folder as the code.
3. Run the script:
   ```bash
   python week2_cyber_storytelling.py
   ```
   or open `week2_clean.ipynb` in Jupyter and choose **Kernel > Restart and Run All**.

## Limitations

- The values are spread very evenly across categories, which suggests the data may be simulated or heavily aggregated. The findings describe this dataset and should not be generalized to the real world without further evidence.
- The analysis shows associations only, not cause and effect, and no statistical significance tests were run.
- Several differences (between attack types and between countries) are modest.

## Author

Sumit Mhalaskar
GitHub: [Sumitmhalaskar](https://github.com/Sumitmhalaskar)
