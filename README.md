# 🚴‍♀️ Bike Sales (& the Hidden Battle with Excel Web)
This project demonstrates end-to-end data analysis skills using Excel Web — from messy raw data to an interactive dashboard that reveals purchasing patterns.

## The Big Question:
Who bought bikes and who didn't? What specific factors made the difference in purchase decisions?

**Key Insights Discovered:**
- Income differences between bike buyers and non-buyers across genders
- Commute distance impact on purchase decisions
- Age demographics driving bike sales

## Dashboard in Action
Here's a look at the dashboard in action. I had to restart this entire project at one point because Excel Web decided slicers from graphs were a no-go, and copying pivot tables between sheets was a pipe dream. The workaround involved placing all pivot tables and visuals on the same sheet.
![Dashboard & Slicers Demo](/docs/assets/demo.gif)

## Tech Stack
- Microsoft Excel: Utilized Excel Web for dashboard development and data analysis.
- VSCode: Used for documentation.
- Terminal: Employed for GitHub troubleshooting.

## Features
- Interactive Dashboard: A single-sheet dashboard visualizing key bike sales insights.
- Dynamic Slicers: Data filtering by marital status, region, and education.
- Key Metrics Visualized: Displays average income by gender and purchase status, commute distance trends, and age demographics.
- Data Cleaning & Preparation: Step-by-step processes for handling duplicates, clarifying columns, formatting numbers, and typo detection.
- Age Bucketing: Custom Excel formulas to categorize age into meaningful brackets.
- Visual Polish: Dashboard visuals were refined for clarity and impact.

## Quick Start
1. See the dashboard in action: Check out demo.gif above
2. Follow the process: Open [Steps-Web.md](docs/Steps-Web.md) for the complete walkthrough
3. Compare datasets: DatasetDirty.xlsx → DatasetClean.xlsx shows the transformation
4. Hit a snag? [Troubleshooting.md](docs/Troubleshooting.md) has solutions for common Excel Web issues

## Project Structure
```bash
bike-sales-dashboard/
├── docs/assets/          # Screenshots and demo GIF
├── DatasetDirty.xlsx     # Original messy data
├── DatasetClean.xlsx     # Cleaned, analysis-ready data
├── Steps-Web.md          # Complete tutorial
├── Troubleshooting.md    # Common issues & solutions
└── README.md            # You are here
```

## License
This project is open-source under the MIT License.

## Get in Touch
For inquiries or professional connections, reach out via my main GitHub profile: [sycstitch](https://github.com/sycstitch)

## Related Projects
Explore other projects:
	- [La Liga Management System](https://github.com/sycstitch/la-liga-management-system) (Spanish, SQL, PHP, Front & Backend)
	- [TrueCar Webscraper & Data Analysis(https://github.com/sycstitch/truecar-webscraper) (ETL, Python, BeautifulSoup, Pandas, Regex)
