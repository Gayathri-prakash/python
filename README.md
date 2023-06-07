# COVID-19 Simulation Readme

This repository contains code for simulating COVID-19 timeseries data and generating a summary plot. The simulation is performed based on Markov chains and takes into account various parameters such as transition probabilities and holding times.

## Prerequisites

Before running the code, make sure you have the following libraries installed:

- `pandas`
- `numpy`
- `datetime`

## Getting Started

To get started, follow these steps:

1. Clone this repository to your local machine.
2. Ensure that the required libraries are installed.
3. Import the necessary functions and modules:

```python
from helper import create_plot
from sim_parameters import TRASITION_PROBS, HOLDING_TIMES
import datetime
import pandas as pd
import numpy as np
```

## Simulating COVID-19 Timeseries Data

To simulate COVID-19 timeseries data, use the `run` function. This function takes the following parameters:

- `countries_csv_name`: The filename of a CSV file containing country-specific data.
- `countries`: A list of countries for which the simulation should be performed.
- `start_date`: The start date of the simulation in the format "YYYY-MM-DD".
- `end_date`: The end date of the simulation in the format "YYYY-MM-DD".
- `sample_ratio`: The sample ratio to reduce the population of each country.

Here's an example of how to use the `run` function:

```python
run('countries_data.csv', ['Country1', 'Country2'], '2022-01-01', '2022-12-31', 10)
```

The function will simulate COVID-19 timeseries data for the specified countries and store the results in a CSV file named `a3-covid-simulated-timeseries.csv`.

## Generating a Summary Plot

To generate a summary plot based on the simulated data, use the `create_plot` function. This function takes two parameters:

- `data_csv_name`: The filename of the CSV file containing the simulated data.
- `countries`: A list of countries for which the summary plot should be generated.

Here's an example of how to use the `create_plot` function:

```python
create_plot('a3-covid-simulated-timeseries.csv', ['Country1', 'Country2'])
```

The function will generate a summary plot based on the simulated data for the specified countries.

## Output

The simulated COVID-19 timeseries data is saved in a CSV file named `a3-covid-simulated-timeseries.csv`. The summary plot is generated and saved as an image file.

## Additional Notes

- The simulation relies on transition probabilities and holding times defined in the `sim_parameters.py` file. Make sure these parameters are appropriately set for your simulation needs.
- The input data for the simulation should be provided in a CSV file with the following columns: "country", "population", "less_5", "5_to_14", "15_to_24", "25_to_64", "over_65". Ensure that your data is formatted correctly.

Feel free to explore and modify the code to suit your specific requirements. If you have any questions or issues, please don't hesitate to reach out.
