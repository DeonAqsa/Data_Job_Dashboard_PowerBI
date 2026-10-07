# Data Job Dashboard w/ Power BI

![Dashboard Overview](/Resources/main_page.png)


[View the resources on the Power BI here](/Resources/Power_BI_Course_Progress_2.pbix)

## Introduction

This is a redesigned version of my earlier data job market dashboard, this time focused on building a more dynamic, interactive experience in Power BI. Using the same 2024 data job postings dataset, this project explores salary trends and in-demand skills through a single dashboard view, with toggle buttons, slicers, and a hidden filter panel that slides in on click.

## Skills Showcased

- **🧮 DAX Measures:** Built measures to power the KPI cards (`Job Count`, `Yearly Salary`, `Hourly Salary`, `Skills Per Job`) and to drive the salary chart depending on which toggle is selected.
- **⚙️ Power Query (M Language):** Used M to clean and transform the raw job postings data behind the scenes, handling data types, blanks, and shaping the skills table for analysis.
- **🔧 Parameters:** Used Power BI parameters to let a single visual switch between Yearly Salary and Hourly Salary views without needing two separate charts.
- **🖱️ Bookmarks & Buttons:** Built a toggle button pair (Yearly Salary / Hourly Salary) to swap chart views, and a separate bookmark-triggered button that slides out a hidden filter panel for deeper filtering.
- **🎚️ Slicers:** Added Job Title and Country slicers at the top for quick, direct filtering alongside the bookmark-based filter panel.
- **📊 Core Charts:** Used bar charts for salary comparison and top skills, and a line chart to track job postings over time.
- **🎨 Dashboard Design:** Moved to a dark-themed, high-contrast layout to make the KPIs and charts stand out more clearly than the previous version.

## Dashboard Overview

### Main Dashboard View

<img width="1150" height="600" alt="Screen Recording 2026-10-06 162309" src="https://github.com/user-attachments/assets/cfd76a26-9944-41af-bae6-122de08b43a8" />

The top of the dashboard holds four KPI cards: **479K total job count**, **$113K median yearly salary**, **$48.00 median hourly salary**, and **4.8 skills per job** on average. Right below the KPIs sit two toggle buttons, Yearly Salary and Hourly Salary, that switch the bar chart beneath it between the two views without changing the page.

#### Yearly / Hourly Salary Toggle
On the Yearly view, Senior Data Scientist ($155,500) and Machine Learning Engineer ($155,000) lead the pack, followed by Senior Data Engineer ($146,500), Software Engineer ($145,000), and Data Engineer ($126,268), all the way down to Data Analyst at the bottom. Switch to Hourly and the order shifts a bit, Machine Learning Engineer takes the top spot at $61.00/hr, followed by Software Engineer ($60.00), Data Engineer and Senior Data Engineer tied at $59.00, then Cloud Engineer and Senior Data Scientist tied at $50.00. Interesting that Senior Data Scientist drops from #1 yearly to further down hourly, likely a sign that yearly roles in that title lean more toward salaried/full-time structures than hourly contracts.

#### Top Skills
Python and SQL are clearly the two most in-demand skills, both well above 60%, followed by a noticeable drop to AWS and Azure. Tools like Excel, Power BI, and Java sit toward the bottom, suggesting Python and SQL are close to must-haves while the rest are more role-dependent.

#### Job Postings Over Time
Drilling into this chart breaks the year down month by month: January (52,924), February (55,336), March (48,385), April (43,799), May (45,651), June (41,692), July (50,760), August (46,951), September (29,806), October (19,041), November (13,719), and December (30,831). The pattern holds up clearly here, postings peak in February, stay relatively steady through the first half of the year, then drop off hard starting September, bottoming out in November before a partial recovery in December. Whatever caused the slowdown in Q4 2024, it hit fast and only started to ease up right at year's end.

### Filter Panel (Bookmark-Triggered)

![Filter Panel](/Resources/filter_pane.png)

Clicking the filter icon in the top right slides in a hidden panel built with a bookmark, without leaving the main page. It adds four extra filters on top of the Job Title and Country slicers: **No Degree Required?**, **Work From Home?**, **Health Insurance Included?**, and **Schedule Type?**, all as dropdowns defaulting to "All." This lets users narrow the dataset down by job quality factors, not just title or location, while keeping the main dashboard clean when the panel isn't open.

## Conclusion

This version builds on the first dashboard by focusing more on interactivity, using DAX, Power Query, parameters, and bookmarks together to let one page do the work of several. It's a step toward designing dashboards that stay simple on the surface but still give users the depth to filter and explore on their own terms.
