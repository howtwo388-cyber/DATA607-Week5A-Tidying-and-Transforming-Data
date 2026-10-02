## Summary

This approach describes the planned process for the Week 5A Tidying and Transforming Data assignment. The original airline delay data are stored in PostgreSQL in the same wide format as the source, including the intentionally missing airline values.

The data will be retrieved from PostgreSQL and prepared in R. The missing airline names will be populated using reproducible code, and the dataset will be transformed from wide to long format so that each observation represents an airline, flight status, and destination.

The analysis will compare Alaska Airlines and AM West using delay percentages rather than only flight counts. First, the overall delay percentage will be calculated for each airline. Then, delay percentages will be compared separately across Los Angeles, Phoenix, San Diego, San Francisco, and Seattle.

Finally, the analysis will examine the difference between the overall results and the city-by-city results. This comparison will help explain how differences in the distribution of flights across destinations can affect the overall performance of each airline.
