# Global Olympic Sports Performance Analysis

**Author:** Abhedya
**Team ID:** EN25CS3010040
**Project Date:** 29 October 2026
**Platform:** Tableau Public
**Project Type:** Olympic sports data analytics and visualization

## Project Overview

Global Olympic Sports Performance Analysis is a Tableau-based analytics project that explores Olympic medal performance, athlete participation, regional medal-efficiency patterns, host-country results, and the relationship between sports-investment level and medal totals.

The project combines four CSV datasets and presents the analysis through seven chart sheets, four KPI sheets, and two interactive dashboards. It aims to make historical Olympic data easier to explore for sports strategists, analysts, and media storytellers.

## Objectives

- Compare total medal counts across countries.
- Examine how total medals awarded changed across Olympic Games.
- Compare average medals per athlete across sport categories.
- Compare the recorded medal-efficiency measure across regions.
- Explore medal totals for host countries.
- Compare medal totals against sports-investment level for each country.
- Summarise participation with headline KPIs.
- Use interactive filters so every chart on a dashboard updates together.

## Datasets

The project uses four CSV datasets, connected directly in Tableau with relationships configured between them.

| Dataset | Description | Size |
|---|---|---|
| `alltime_country_rankings.csv` | Country-level historical summary: country, NOC code, region, games entered, summer and winter medals, gold/silver/bronze totals, medal points, overall rank, average efficiency | 60 rows, 13 fields |
| `athletes.csv` | Athlete-level records: athlete ID, name, country, gender, sport, sport category, first and last Games year, medal counts, and physical attributes | *(add row and field count)* |
| `games_summary.csv` | One row per Olympic Games: year, season, host city and country, participating nations, total athletes, total medals awarded, top country | 18 rows, 10 fields |
| `medal_results.csv` | Country-per-Games medal records: year, host country, host-nation flag, region, GDP tier, sports investment, investment score, medal efficiency %, and gold/silver/bronze/total medals | 910 rows, 20 fields |

**Dataset folder (Google Drive):** https://drive.google.com/drive/folders/14ADnfQBo6f-0PRFCLOhjUYCdGHG70Ohx?usp=sharing

## Technology Stack

- **Data source:** CSV files
- **Visualization and analytics:** Tableau Public
- **Interactive controls:** Dashboard filters (country, year, sport category, region, host country)
- **Repository:** GitHub

## Visualizations

The workbook contains seven chart sheets:

1. **Avg Medals per Athlete by Sport Category** — horizontal bar chart ranking sport categories by average medals per athlete.
2. **Global Performance Metrics by Country** — top 10 countries by total medals (United States 735, China 696).
3. **Trend of Total Medals Awarded Over the Years** — line chart across 18 Games from 1992 to 2026, ranging from a low of 305 (2000) to a peak of 363 (2020), with 334 in 2026.
4. **Global Sports Investment vs. Medal Performance** — bubble chart of 60 countries. Average investment score is on the x-axis, total medals on the y-axis, bubble size shows average medal efficiency, and colour shows region.
5. **Avg Medal Efficiency % by Region** — pie chart. South America is highest at 49.64, followed by Europe/Asia at 45.98 and Africa at 42.80.
6. **Comparing Medal Totals Across Olympic Hosts** — bar chart of host countries ranked by total medals at Games they hosted (filtered to Host Nation = 1).
7. **Regional Medal Efficiency and Distribution by Sport** — donut chart of total medals split by region.

## KPI Sheets

| KPI | Value |
|---|---|
| Global Athlete Participation | 910 |
| Total Sports Categories Entered | 60 |
| Total Nations Represented | 18 |
| Regional Performance Efficiency | about 33.2 |

See the Limitations section for how these KPIs are calculated.

## Tableau Public Dashboards

### Dashboard 1 — Global Sports Performance Analytics Dashboard

URL: https://public.tableau.com/shared/D27ZZ432G?:display_count=n&:origin=viz_share_link

Includes:

- KPI row: Global Athlete Participation, Total Sports Categories Entered, Total Nations Represented
- Total medal achievements across nations (map)
- Trend of Total Medals Awarded Over the Years
- Avg Medals per Athlete by Sport Category
- Global Performance Metrics by Country
- Filters for country, year and sport category

### Dashboard 2 — Olympic Performance and Regional Efficiency Dashboard

URL: https://public.tableau.com/views/OlympicRecord_17931226176910/Story1?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

Includes:

- KPI row: Regional Performance Efficiency and participation summary tiles
- Average Medal Efficiency Percentage by Region (pie)
- Global Sports Investment vs. Medal Performance (bubble)
- Comparing Medal Totals Across Olympic Hosts
- Regional Medal Efficiency and Distribution by Sport (donut)
- Filters for region and host country

Both dashboards use a dark teal background with gold and white title text, a title banner, KPI tiles at the top, a structured chart grid, and filter panels on the right-hand side that update all charts at once.

## Project Demonstration

Demonstration video: https://drive.google.com/file/d/1rofwXEJ0USrBcDlRSo3qFCit9ufnvbMA/view

## How to Explore the Project

1. Open either dashboard URL above.
2. Use the filter panels on the right to change the data shown.
3. Hover over marks for tooltips, such as country names on the bubble chart.
4. Compare countries, regions, host countries, and investment levels across the charts.

## Key Takeaways

- Total medals awarded per Games stays within a fairly narrow band (305 to 363) across the 18 Games, with no steady upward trend.
- The United States (735) and China (696) lead on total medals among the top 10 countries.
- South America has the highest average medal-efficiency value (49.64), and Europe/Asia is next (45.98).
- Countries in the highest investment group (score 3) include the largest medal totals, though many countries in that group have much smaller totals.

## Limitations

- Findings depend on the coverage, structure, and definitions in the supplied datasets.
- The investment-level comparison shows a pattern in the available data and does not prove that spending causes medal success.
- Host-country comparisons alone do not establish that hosting caused a country's medal performance.
- The Hosts sheet filters to Host Nation = 1, so each bar shows a host country's own medals at Games it hosted. For example, Japan is 51, from two Games (24 and 27 medals). These values come directly from `medal_results.csv`.
- The KPI "Total Nations Represented" counts rows in `games_summary.csv`, so its value of 18 is the number of Games editions. The KPI "Total Sports Categories Entered" is a distinct count of NOC codes, giving 60 countries.
- This is a Tableau analytics and visualization project. No separate web application is included.

## Future Scope

- Add more recent, verified Olympic data when suitable datasets become available.
- Expand the analysis with further sport, country, and time-period comparisons.
- Document metric definitions and data-preparation steps in more detail.
- Add athlete gender and participation views by sport.

## GitHub Repository

https://github.com/abby0406/Global_Olympic_Sports_Analysis
