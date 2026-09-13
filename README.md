# BERN02

## About

This repository contains implementations and experiments for different statistical modelling methods.

Currently, the repository includes:

- Local Regression — simple local regression using one predictor on an air pollution dataset.
- Poisson Regression — regression for modelling bird count data using a Poisson response distribution.

Additional statistical methods and models may be added to the repository over time.

## Data

For the modelling data from <a href="https://github.com/luchem/bern02"> is utilized.

The original dataset is licensed under the Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0) license.

For more information, see the <a href="https://github.com/luchem/bern02/blob/main/LICENSE"><u> CC BY-SA 4.0 license</u></a>.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Content

- 'Task_1_Regression/': 
  - `local_regression.ipynb`: Here the local regression is implemented and applied to the air pollution dataset <a href= "https://github.com/Chardes01/BERN02/blob/main/Task_1_Regression/Task_1_Regression/pollution_cleaneddata.csv"><u>pollution dataset</u></a> and results are visualized.
  - `pollution_cleaneddata.csv`: Dataset used for the task and only the following variables:
    - Total age-adjusted mortality rate per 100,000 (MORT)
    - families with income <3000$ (POOR)
 
- 'Task2_Poisson_regression/': Here the files for modelling a Poisson regression based on bird count data are provided.
  - `Task2.ipynb`: Here the Poisson regression is applied on the <a href= "https://github.com/Chardes01/BERN02/blob/main/Task_2_Poisson_regression/bird_count.csv"><u>bird count dataset</u></a>.
  - `bird_count.csv`: The bird count dataset.


## Prerequisites

Install [uv](https://docs.astral.sh/uv/) before setting up the project.

## Installation

Clone the repository and navigate to the project directory:

```bash
git clone <repository-url>
cd <project-directory>
```

Create the virtual environment and install all required dependencies:

```bash
uv sync
```

The required Python version and dependencies are specified in `pyproject.toml`. The `uv.lock` file ensures that the same dependency versions are installed.

## License

Distributed under the MIT License. See `LICENSE.txt` for more information.
