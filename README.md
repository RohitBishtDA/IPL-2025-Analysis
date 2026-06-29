# 🏏 IPL 2025 Analysis

> End-to-end Exploratory Data Analysis of IPL 2025 using Python

---

## 📌 Project Overview

This project performs a comprehensive analysis of **IPL 2025** season data — covering batting, bowling, team performance, toss impact, and a custom **Impact Score** model to identify the most valuable players of the tournament.

---

## 📂 Dataset

| Detail | Info |
|--------|------|
| **Files Used** | `matches.csv`, `deliveries.csv`, `orange_cap.csv`, `purple_cap.csv` |
| **Records** | Ball-by-ball delivery data for entire IPL 2025 season |
| **Source** | Kaggle |

---

## 🛠️ Tools & Libraries

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading, cleaning, groupby aggregations |
| `numpy` | Numerical operations |
| `matplotlib` | Chart rendering |
| `seaborn` | Statistical bar plots |

---

## 🧹 Data Cleaning Steps

- Removed incomplete/draw matches (`match_result != 'completed'`)
- Filled nulls in `wicket_type`, `player_dismissed`, `fielder` with `'none'`
- Engineered new columns: `is_wicket`, `is_four`, `is_six`, `legal_ball`
- Saved cleaned files as `matches_clean.csv` and `deliveries_clean.csv`

---

## 🔍 Analysis Performed

**Batting**
- Top 10 Run Scorers
- Top 10 Strike Rates (min. 200 balls faced)
- Top 10 Six Hitters
- Top 10 Four Hitters

**Bowling**
- Top 10 Wicket Takers
- Top 10 Best Economy Rates (min. 60 balls bowled)
- Top 10 Dot Ball % Bowlers

**Team & Match**
- Win % by Team
- Toss Impact on Match Result
- Bat First vs Bowl First Win %
- Average Runs Per Over

**Custom Model**
- 🏆 Top 10 Most Impactful Players (custom Impact Score using Runs + SR + Wickets + Economy + Catches)

---

## 📊 Visualizations

### 🏆 Top 10 Run Scorers
![Top 10 Run Scorers](https://github.com/user-attachments/assets/c34f6b6c-f2d3-4c53-9a44-4bbb7f117df4)

### ⚡ Top 10 Strike Rates
![Top 10 Strike Rates](https://github.com/user-attachments/assets/387386e7-1ea8-4e36-95be-7f8d2abba67c)

### 💥 Top 10 Six Hitters
![Top 10 Six Hitters](https://github.com/user-attachments/assets/a1765565-6ad5-4a06-8bb1-0a660226f6e2)

### 4️⃣ Top 10 Four Hitters
![Top 10 Four Hitters](https://github.com/user-attachments/assets/0db41115-d422-47c4-b73f-0f8ded271193)

### 🎯 Top 10 Wicket Takers
![Top 10 Wicket Takers](https://github.com/user-attachments/assets/89f6f012-3f1d-41c7-a579-55a63efa9820)

### 💰 Top 10 Best Economy Rates
![Best Economy Rates](https://github.com/user-attachments/assets/fc5d68ed-32e2-41d9-9621-315e9d53d881)

### 🔴 Top 10 Dot Ball %
![Dot Ball %](https://github.com/user-attachments/assets/3b8fdbf0-4333-4e88-b08b-2e0841870729)

### 📈 Average Runs Per Over
![Avg Runs Per Over](https://github.com/user-attachments/assets/c68dbf7a-9e9f-4e0a-ad3a-4ee48b294b5b)

### 🏅 Win % by Team
![Win % by Team](https://github.com/user-attachments/assets/26b918cd-3239-4234-adf3-117c0dcc7f54)

### 🎲 Toss Impact on Match Result
![Toss Impact](https://github.com/user-attachments/assets/bbef479a-1304-4e1b-8705-6b11bb1ff92d)

### 🏏 Bat First vs Bowl First Win %
![Bat vs Bowl First](https://github.com/user-attachments/assets/1eebc68e-69cf-48f1-bf95-d372221a3d8a)

### 🌟 Top 10 Most Impactful Players
![Most Impactful Players](https://github.com/user-attachments/assets/a6e1cf06-4690-4f49-afdd-74b04b2bf6a9)

---

## 🧮 Custom Impact Score Model

A self-designed scoring model to rank players holistically across batting, bowling, and fielding.

### Batting
- **Run Points** = Total runs scored
- **Strike Rate Points** — SR ≥ 200 → +50 | SR ≥ 170 → +35 | SR ≥ 150 → +20 | SR ≥ 130 → +10 | SR < 120 → -50
- Minimum 50 balls faced required to qualify

### Bowling  
- **Wicket Points** = Wickets × 30
- **Economy Points** — Eco < 8 → +50 | Eco < 9 → +35 | Eco < 10 → +20 | Eco ≥ 15 → -50
- Minimum 100 balls bowled required to qualify

### Fielding
- **Catch Points** = Catches × 5

### Formula
`Impact Score = Run Points + SR Points + Wicket Points + Economy Points + Catch Points`

## 💡 Key Insights

- 🏏 Top run scorers and six hitters dominate with explosive strike rates
- 🎯 Best economy bowlers maintain under 8 runs/over in legal deliveries
- 🎲 Toss impact analysis reveals whether batting/bowling first holds a winning edge
- 🌟 Custom **Impact Score** model combines batting, bowling & fielding — giving a holistic view beyond just runs or wickets
- 📈 Average runs per over chart shows powerplay vs death over trends

---

## 📬 Contact

**Author:** Rohit Singh Bisht  
**Email:** Rohitsinghbishtkv@gmail.com
