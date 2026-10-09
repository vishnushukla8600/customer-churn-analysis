# Customer Churn Analysis

Exploratory analysis of a subscription-business customer churn dataset (**64,374 customers, 12 columns**), with business insights and retention recommendations.

## Key findings
- **Payment delay is the strongest churn signal:** churn rises from 10% (0-10 days late) to 39% (11-20 days) and 77% (21-30 days).
- **Heavy support contact predicts churn:** customers with 5+ support calls churn at about 61%, versus 23-29% for 4 or fewer.
- **Delay and support calls compound:** more than 4 calls and more than 20 days delay gives 89% churn; neither gives 5%.
- **Highest-risk segments:** female customers (55% vs 39% male) and monthly-contract customers.
- **Plan tier and last-interaction recency barely matter.**
- **Data-quality warning:** churn is about 26% for CustomerID up to 40,000 and about 83% above, which suggests two datasets stacked together.

## Recommendations
1. Fix billing friction: reminders, autopay incentives, flexible due dates.
2. Flag customers with delay above 20 days or more than 4 support calls for a retention team.
3. Improve first-contact resolution in support.
4. Re-engage low-usage and long-tenure customers.
5. Move monthly customers to longer contracts and investigate the gender gap.

## Repository contents
| Path | Description |
|---|---|
| `Customer_Churn_Analysis.ipynb` | Full analysis notebook (dataset understanding, preparation, EDA, engagement, retention, satisfaction proxies, visualisation) |
| `Churn_Insights_and_Recommendations.docx` | Written report of insights and recommendations |
| `visualizations/` | Final charts (distributions, churn drivers, heatmaps) |
| `screenshots/` | Screenshots of each analysis step |
| `requirements.txt` | Python dependencies |

## How to run
```bash
git clone https://github.com/YOUR-USERNAME/customer-churn-analysis.git
cd customer-churn-analysis
pip install -r requirements.txt
jupyter notebook Customer_Churn_Analysis.ipynb
```
Place `Training_dataset_for_customer_churn.csv` in the project root before running the notebook.

## Notes
- The original brief mentioned learning hours, completion rate and satisfaction score. This dataset has none of them, so each was mapped to a churn equivalent (engagement = Usage Frequency / Last Interaction; satisfaction proxies = Support Calls and Total Spend; platform = Subscription Type / Contract Length).
- Findings are associations, not proven causes.

## Tools
Python, pandas, NumPy, Matplotlib, Seaborn, Jupyter.
