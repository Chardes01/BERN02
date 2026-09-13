# BERN02

## About The Project

In this repository code is provided ...

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Content

- 'Task_1_Regression/':  Here the files for modelling local regression for ....
  - `local_regression.ipynb`: Here the regression is applied to the pollution dataset <a href= "https://github.com/Chardes01/BERN02/blob/main/Task_1_Regression/Task_1_Regression/pollution_cleaneddata.csv"><u>pollution dataset</u></a> and results are visualized.
  - `pollution_cleaneddata.csv`: Dataset used for the task (we only use the parameters "MORT" and "POOR", which are the ...
 
- 'Task2_Poisson_regression/': Here the files for modelling a Poisson regression based on bird count data are provided.
  - `Task2.ipynb`: Here applied on the <a href= "https://github.com/Chardes01/BERN02/blob/main/Task_2_Poisson_regression/bird_count.csv"><u>bird count dataset</u></a>.
  - `bird_count.csv`: The dataset. We are especially interested in 'Yr' (Year) and 'count'


## Prerequisites

To run this code install * [uv](https://docs.astral.sh/uv/)


## Setup

Create the virtual environment and install the project dependencies:

```bash
uv sync
```

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
