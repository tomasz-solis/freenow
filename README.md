# FREE NOW Driver-Engagement Analysis 📊

*Author:* **Tomasz Solis**  
*Last updated:* 2025-06-22  


## 1 · Project structure
```text
.
├── data/
│   ├── freenow_drivers.csv
│   ├── freenow_drivers_activity.csv
│   └── freenow_drivers_campaign.csv
├── FN_SDA_TomaszSolis.ipynb      # analysis & visuals – runnable top-to-bottom
└── README.md                     # this file
```
## ⚙️ Quick-start

# 1 – Clone repo & enter folder
git clone <repo_url>

# 2 – Create virtual env & install deps
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt     

# 3 – Open notebook
jupyter lab notebooks/FN_SDA_TomaszSolis.ipynb


## Data sources

| File                             | Rows  | Description                                     |
| -------------------------------- | ----: | ----------------------------------------------- |
| `freenow_drivers.csv`            | 50 k  | Driver master attributes                        |
| `freenow_drivers_activity.csv`   | 1.8 M | Daily activity summary                          |
| `freenow_driver_campaign.csv`    | 10 k  | A/B campaign groups & post-week ride counts     |

<sub>*All PII removed; IDs pseudonymised.*</sub>



## Recommendations

- **Gamify streaks** – in-app badge & “days left to keep gold” countdown (+0.3-0.6 rides)
- **Opt-in recovery flow** – close ~30 % engagement gap from marketing optPush hot-spot alerts (+2 rides)
- **Push hot-spot alerts** - as in app or push notifications (+2 rides) 

---

## Risks

- Retention < 12w
- Taxi backlash → monitor earnings spread
- Weekly RPD dashboard monitoring

---

## 🤝 Contact

Questions, ideas, or 🔍 audit requests → **tomasz.solis@gmail.com**

<br>

*Made with ❤️ pandas & Plotly.*
