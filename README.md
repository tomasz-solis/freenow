# FREE NOW Driver-Engagement Analysis 📊
Senior-level exploratory & causal analysis of FREE NOW driver behaviour for the Supply Product team.  

*Author:* **Tomasz Solis**  
*Last updated:* 2025-06-22  

---

## 🚀 Project goals
1. **Define & monitor engagement KPIs** – rides / active-driver-day, acceptance, completion.  
2. **Uncover behavioural drivers** – gold streaks, marketing opt-in, vehicle type.  
3. **Measure causal impact** of the Jun-2020 demand-forecast email (A/B + diff-in-diff).  
4. Deliver **actionable recommendations** for product nudges & future experiments.  

---

## 📂 Repository structure
```text
.
├─ CSVs/
│   ├─ freenow_drivers.csv
│   ├─ freenow_drivers_activity.csv
│   └─ freenow_driver_campaign.csv
├── notebooks/
│   └── FN_SDA_TomaszSolis.ipynb
├── requirements.txt       
└── README.md
```
## ⚙️ Quick-start

# 1 – Clone repo & enter folder
git clone <repo_url>
cd freenow-driver-analysis

# 2 – Create virtual env & install deps
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt     

# 3 – Open notebook
jupyter lab notebooks/FN_SDA_TomaszSolis.ipynb



## 📊 Data sources

| File                             | Rows  | Description                                     |
| -------------------------------- | ----: | ----------------------------------------------- |
| `freenow_drivers.csv`            | 50 k  | Driver master attributes                        |
| `freenow_drivers_activity.csv`   | 1.8 M | Daily activity summary                          |
| `freenow_driver_campaign.csv`    | 10 k  | A/B campaign groups & post-week ride counts     |

<sub>*All PII removed; IDs pseudonymised.*</sub>

## 🧪 Methodological highlights

- **Schema guard** – asserts required columns on load.  
- **Typed, unit-tested helpers** – `summarise_monthly`, retention builder.  
- **Diff-in-diff** – controls for pre-campaign activity; Welch t-test for robustness.  
- **Cohort retention** – cumulative share of cohort active, faceted by signup year.  
- **Plotly visuals** – colour-blind palette, hover metrics, interactive facets.  

---

## 📈 Key results

| KPI | Pre-COVID<br>(Feb-20) | Trough<br>(Apr-20) | Latest<br>(Jun-20) |
| --- | :----: | :----: | :----: |
| **Rides / active driver / day** | 2.0 | 0.7 | 1.5 |
| **Offer acceptance rate** | 27 % | 51 % | 43 % |
| **Completion rate** | 82 % | 83 % | 83 % |

* Email campaign delivers **+2.0 rides / driver** (95 % CI ± 0.4) after diff-in-diff.  
* Each extra **gold streak** → **+0.8 rides / day** (*p* < 0.001).

*See notebook for full visuals & commentary.*

---

## 📝 Recommendations

- **Gamify streaks** – in-app badge & “days left to keep gold” countdown.  
- **Opt-in recovery flow** – close ~30 % engagement gap from marketing opt-outs.  
- **Scale demand-forecast push** – move from weekly email to geo-targeted app push.  
- **Weekly KPI alerting** – flag dips below 1.4 rides / driver / day.

---

## 🚧 Limitations & next steps

- Dataset ends **2020-06-30** → long-term retention unobserved.  
- No revenue fields → cannot compute driver LTV.  
- Future: **causal-impact model** for continuous forecast-push rollout.

---

## 🤝 Contact

Questions, ideas, or 🔍 audit requests → **tomasz.solis@gmail.com** or Slack **#supply-insights**.

<br>

*Made with ❤️ pandas & Plotly.*
