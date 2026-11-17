# 🚦 Road Accidents Dashboard (2022-2025)

An interactive Power BI dashboard that shows **when, where and in what
conditions road accidents happen**, built from 20,000 accident records.

![Overview](screenshots/overview.png)
![Deep dive](screenshots/deep_dive.png)

## 🎯 Why I built this
Road accidents affect everyone. I wanted to turn raw data into something
simple that shows which conditions are the riskiest, so people can
plan better safety steps.

## 🛠️ Tools used
| Tool | What I used it for |
|---|---|
| Python (Pandas) | Cleaning the data |
| Power BI | Building the dashboard |
| DAX | Creating the Fatal % measure |

## 🧹 What I did
1. Cleaned the raw data in Python and removed columns I didn't need
2. Fixed the `hour` column (it was all 0), so I rebuilt it from the `time` column
3. Built a 2-page dashboard in Power BI
   - **Overview:** totals, severity, weather, road type, day of week, monthly trend
   - **Deep dive:** accidents by day and hour (heatmap) and Fatal % by day

## 🔍 Key findings
- **Fog is the riskiest weather.** Average risk score: fog 0.59, rain 0.49, clear 0.24
- **Heavy traffic means higher risk.** High traffic density scores 0.59, low scores 0.34
- **Fatal accidents are about 15% of all accidents.** Minor 55%, major 30%, fatal 15%
- **Sunday has the highest fatal rate (15.9%)**, Thursday the lowest (14.2%).
  The gap is small, so the day matters less than weather and traffic
- **Urban, rural and highway roads** have almost equal numbers of accidents (about 33% each)

## 💡 Suggestions
- Add fog warnings and speed limits on risky roads
- Put more patrols at peak accident hours

## ⚠️ Note
The 2025 data is **partial**, so the drop in the 2025 line is not a real trend.

## 📂 Files in this repo
- `road_accidents_dashboard.pbix`: the Power BI file (open with Power BI Desktop)
- `road_accidents_dashboard.pdf`: view both pages without Power BI
- `accidents_final.csv`: cleaned data
- `[your notebook name].ipynb`: Python cleaning steps
- `screenshots/`: dashboard images

## 🚀 How to open it
1. Download the `.pbix` file
2. Open it in Power BI Desktop (free)
3. Click the year and road type buttons to explore
