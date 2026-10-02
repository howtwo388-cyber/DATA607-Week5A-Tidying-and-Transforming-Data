# DATA 607 Week 5A – Tidying and Transforming Data

## Airline Delays Analysis

This project was completed for DATA 607 – Data Acquisition and Management.

The project analyzes airline arrival performance for Alaska Airlines and AM West across five U.S. cities:

- Los Angeles
- Phoenix
- San Diego
- San Francisco
- Seattle

The original dataset contains counts of on-time and delayed flights. It is provided in wide format and includes missing airline values that must be preserved in the recreated source data and then populated using reproducible code.

## Project Objectives

The main objectives of this project are to:

- Recreate the original airline data, including the missing values.
- Store and retrieve the original data using PostgreSQL.
- Populate the missing airline information using R.
- Transform the dataset from wide to long format.
- Analyze flight counts and delay percentages.
- Compare the overall delay percentages of Alaska Airlines and AM West.
- Compare the airlines' delay percentages across all five cities.
- Examine the difference between the overall and city-by-city results.
- Explain how the distribution of flights across destinations affects the overall comparison.

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

The final comparison examines why the overall results may differ from the city-by-city results.

## Tools

- R
- Quarto
- PostgreSQL
- RPostgres
- DBI
- dplyr
- tidyr
- ggplot2
- knitr

## Repository Contents

- `airline_delays.csv` – recreated original airline dataset
- `DATA607-Week5A-Airline-Delays.qmd` – reproducible Quarto source
- `DATA607-Week5A-Airline-Delays.html` – rendered report
- `_quarto.yml` – Quarto project configuration

## Author

Patricio Romero  
DATA 607 – Data Acquisition and Management
