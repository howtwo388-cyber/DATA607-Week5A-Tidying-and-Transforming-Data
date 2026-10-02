# DATA 607 Week 5A – Tidying and Transforming Data

## Airline Delays Analysis

This project was completed for DATA 607 – Data Acquisition and Management.

The project analyzes airline arrival performance for Alaska Airlines and AM West across five U.S. cities:

- Los Angeles
- Phoenix
- San Diego
- San Francisco
- Seattle

The original dataset was provided by the instructor as an image. Because the source data were not available in a machine-readable format, the table was manually recreated as `airline_delays.csv`, preserving the original structure, flight counts, and missing airline values.

The recreated CSV file was then imported into PostgreSQL using pgAdmin 4. The SQL used to create the PostgreSQL table is documented in the Quarto report for reproducibility. R is used to retrieve, tidy, transform, validate, and analyze the data.

## Project Objectives

The main objectives of this project are to:

- Recreate the original airline dataset from the instructor-provided image.
- Preserve the missing values that appeared in the original source.
- Store the recreated data in PostgreSQL using pgAdmin 4.
- Document the SQL used to create the PostgreSQL table.
- Retrieve the original wide-format data from PostgreSQL using R.
- Populate the missing airline information using reproducible R code.
- Transform the dataset from wide to long format.
- Validate the transformed dataset.
- Analyze flight counts and delay percentages.
- Compare the overall delay percentages of Alaska Airlines and AM West.
- Compare the airlines' delay percentages across all five cities.
- Examine the difference between the overall and city-by-city results.
- Explain how the distribution of flights across destinations affects the overall comparison.

## Data Workflow

The project follows this reproducible workflow:

**Instructor-provided image → Recreated CSV → pgAdmin 4 → PostgreSQL → R → Data Tidying → Analysis**

The original observations are stored in PostgreSQL in their recreated wide format. The two missing airline values are intentionally preserved in the database and are populated later using reproducible R code.

## PostgreSQL Database

The recreated `airline_delays.csv` file was imported into the PostgreSQL database:

`data607_week5a`

The source observations are stored in:

`public.airline_delays_raw`

The table contains a generated `record_id`, the airline and flight-status fields, and the flight counts for the five destinations.

The SQL table-creation code is included in the Quarto report to document the database structure and make the database portion of the project reproducible.

## Analysis

Airline performance is evaluated using percentages rather than only raw flight counts.

The delay percentage is calculated as:

$$
\text{Delay Percentage} =
\frac{\text{Delayed Flights}}
{\text{On-Time Flights} + \text{Delayed Flights}}
\times 100
$$

The analysis compares the two airlines at two levels:

1. Overall airline performance.
2. Airline performance within each of the five destinations.

The final comparison examines why the overall results may differ from the city-by-city results and how the distribution of flights among destinations can affect the overall percentages.

## Tools

- R
- Quarto
- PostgreSQL
- pgAdmin 4
- RPostgres
- DBI
- dplyr
- tidyr
- ggplot2
- knitr
- GitHub
- RPubs

## Repository Contents

- `airline_delays.csv` – manually recreated source dataset preserving the original missing values
- `DATA607-Week5A-Airline-Delays.qmd` – reproducible Quarto source, including PostgreSQL SQL documentation
- `DATA607-Week5A-Airline-Delays.html` – rendered HTML report
- `_quarto.yml` – Quarto project configuration
- `README.md` – project documentation

## Published Report

RPubs:

https://rpubs.com/howtwo3/1464471

## Author

Patricio Romero  
DATA 607 – Data Acquisition and Management
