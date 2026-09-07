# COVID-19 Global Tracker

A Jupyter notebook that analyses global COVID-19 cases, deaths and vaccination
progress over time and compares them across countries.

## What it does

- Loads and cleans the Our World in Data COVID-19 dataset
- Tracks cases, deaths and vaccinations over time for Kenya, the United States
  and India
- Compares the three countries on death rate and share of population vaccinated
- Draws line charts, bar plots and two world choropleth maps
- Sets out the findings in the notebook alongside the code

## Built with

Python 3.13, pandas, seaborn, matplotlib, plotly.express, nbformat

## How to run it

1. Download `owid-covid-data.csv` from
   https://github.com/owid/covid-19-data/blob/master/public/data/owid-covid-data.csv
   (about 100 MB, so it is not in this repository).
2. Put the file in the project folder.
3. `pip install -r requirements.txt`
4. Open `covid_tracker.ipynb` in Jupyter and run all cells.

## What I found

- The United States recorded the most cases (103.4 million) and deaths (1.19
  million), then India (45.0 million and 534 thousand), then Kenya (344
  thousand and 5.7 thousand).
- Deaths as a share of confirmed cases were highest in Kenya at 1.65 percent,
  against 1.18 percent for India and 1.15 percent for the United States.
- The tallest wave in the whole period was the United States in January 2022,
  at about 800 thousand new cases a day on a 7-day average. India's largest
  wave was in the first half of 2021, near 400 thousand a day.
- India shows 67 percent of its population fully vaccinated at the latest
  date. Kenya and the United States show zero, which is a defect in the
  cleaning step, not a fact: their latest rows carry no vaccination value and
  the notebook fills missing values with zero. The fix is to take the last
  reported value per country. It is noted in the findings cell and is the next
  change I would make.

## Screenshots

![Total cases over time](docs/total_cases.png)

![Daily new cases, 7-day average](docs/new_cases_7day.png)

## Data

Data from Our World in Data.

## Licence

MIT

## Author

Rehumile Masego Sechele, rehumiles@gmail.com
