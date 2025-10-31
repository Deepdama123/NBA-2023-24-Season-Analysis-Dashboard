# NBA 23-24 Season Analysis - Power BI Dashboard

[cite_start]This project is a comprehensive Power BI analysis of the NBA 2023-2024 season[cite: 5]. It provides a high-level overview of league-wide performance, detailed team comparisons, and a deep dive into individual player statistics.

## 📊 Dashboard Showcase

The dashboard is organized into four main pages:

### 1. Season Performance Overview
<img width="1323" height="741" alt="image" src="https://github.com/user-attachments/assets/b177af86-13f0-48e9-8756-7e13d6071e16" />


* **Key Performance Indicators (KPIs):**
    * [cite_start]**Total Games Played:** 2460 [cite: 10]
    * [cite_start]**Total Points Scored:** 561.92K [cite: 11]
    * [cite_start]**Total Three Pointers:** 63K [cite: 12, 13]
    * [cite_start]**Total Rebounds:** 144K [cite: 14] (Note: The label says "Totswolarters", likely a typo for Total Rebounds)
    * [cite_start]**Total Assists:** 131K [cite: 17, 19]
    * [cite_start]**Total Steals:** 37K [cite: 20]
    * [cite_start]**Total Blocks:** 25K [cite: 21]
    * [cite_start]**Total Turnovers:** 63K [cite: 22, 23]
* **Visualizations:**
    * [cite_start]**Average Points and Total Games Played Over Time:** A line chart tracking scoring trends throughout the season[cite: 24, 49].
    * [cite_start]**Team Wins and Losses Comparison:** A bar chart comparing the win/loss records of various teams[cite: 29, 76].
    * [cite_start]**NBA Team Player Locations:** A map visualizing the geographical distribution of team players[cite: 15].

### 2. Team Performance Comparison
<img width="1323" height="742" alt="image" src="https://github.com/user-attachments/assets/ec58cf1f-f701-4de4-9710-8b092dbe2db7" />


* **Visualizations:**
    * [cite_start]**Team Selection:** Slicers to filter teams by name and strength (e.g., Strong, Average, Weak)[cite: 40, 50, 89].
    * [cite_start]**Average Team Performance Metrics:** A bar chart comparing teams across metrics like Average Points, Field Goals, Turnovers, Steals, and Blocks[cite: 95, 96].
    * [cite_start]**Average Offensive Rebounds and Total Rebounds by Team:** A radar chart showing rebounding prowess[cite: 82, 83].
    * [cite_start]**Distribution of Average Assists by Team:** A pie chart breaking down the league's assist distribution by team[cite: 109].

### 3. Player Performance Comparison by Team

<img width="1324" height="747" alt="image" src="https://github.com/user-attachments/assets/4fd4c639-3644-413f-b1ce-98f3af949b21" />


* **Visualizations:**
    * [cite_start]**Player Performance Summary:** A detailed table listing each player's position, total points, assists, rebounds, and a calculated "Performance Score"[cite: 121, 122].
    * [cite_start]**Top Players by Performance Metrics:** A treemap identifying the most impactful players on the roster[cite: 123].
    * **Donut Charts:**
        * [cite_start]**Sum of Two-Point Field Goals Per Game by Player** [cite: 213]
        * [cite_start]**Sum of Total Steals by Player** [cite: 219]
        * [cite_start]**Sum of Total Minutes Played by Player** [cite: 227]

### 4. Top Player Performance Comparison

<img width="1324" height="746" alt="image" src="https://github.com/user-attachments/assets/b961597a-f5ab-4c50-9c17-45d308617a06" />


* **KPIs:**
    * [cite_start]**Total Points:** 222K [cite: 271, 273]
    * [cite_start]**Total Assists:** 51K [cite: 282, 285]
    * [cite_start]**Total Blocks:** 9582 [cite: 289, 291]
* **Visualizations:**
    * [cite_start]**Player Statistics by Team and Position:** A table ranking top players like Donovan Mitchell, Jayson Tatum, and Joel Embiid by their Performance Score[cite: 249, 272, 275, 278, 284].
    * [cite_start]**Shooting Efficiency Comparison:** A radial chart comparing players on shooting percentages (Field Goal %, Three Point %, Free Throw %)[cite: 250, 251].
    * [cite_start]**Player Efficiency Rating by Rank and Position:** A bar chart analyzing efficiency across different player positions (c, pf, pg, sg, sf)[cite: 293, 294].
    * [cite_start]**Total Points vs. Total Assists by Player Position:** A scatter plot identifying outliers and trends in scoring and playmaking[cite: 307].

---

## ⚙️ Data Model

The dashboard is built on a data model designed to connect player, team, and game statistics.


* **NBA_Teams:** A dimension table containing team information like `Team_Name`, `Team_Abr`, `Team_Strength`, and `TeamLosses`. It connects to `NBA_Games`, `NBA_Player`, and `NBA_Logo`.
* **NBA_Player:** A dimension table with individual player details such as `FirstName`, `LastName`, `BirthDate`, `Height`, and `Country`.
* **NBA_Games:** A fact table holding game-level data, including `Assists`, `Blocks`, and `Date`.
* **NBA_Roster:** A dimension table with player roster information like `College`, `City`, and `Country`. It has a one-to-one relationship with `NBA_Player`.
* **NBA_Logo:** A dimension table that links a `Team_Name` and `Team_Index` to an `ImageURL` for displaying team logos.
* **Top 5 Players by Pos...:** A calculated or summary table showing aggregated stats like `Assists per Game`, `Blocks per Game`, and `Field Goal Percentage`.

---

## 🛠️ Tools Used

* **Microsoft Power BI:** Used for data modeling, DAX calculations, and interactive data visualization.
