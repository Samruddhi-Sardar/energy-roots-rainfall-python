# Energy, Roots, and Rainfall: Applied Python Modelling Portfolio

A personal coursework project built for **MATH6005/6182 Assignment 1** (University of Southampton), focused on turning mathematical models into practical Python workflows.

## Project Snapshot
This repository presents my end-to-end work on three applied modelling problems:
- household electricity consumption simulation,
- iterative nonlinear root-finding,
- weather-driven rainfall probability analysis.

The work combines mathematical formulation, numerical methods, and data visualization using Python and Jupyter.

## Assignment Context
- Module: `MATH6005 / MATH6182`
- Weighting: `20%`
- Submission date: `18 November 2024`
- Submission format: single Jupyter Notebook

## What I Built

### 1) Household Electricity Consumption Model (40 marks)
I implemented and analyzed the model:

`U(t) = (B + C(t) + f(A,t)) * F(t)`

using:
- `B = 50`, `kappa = 0.1`, `A = 5`
- occupant profile: `uM = 1.5`, `uE = 2.0`, `uoff = 0.5`
- `F(t) = 1.2` (weekdays), `0.8` (weekends)

Deliverables completed:
- simulated a 28-day random temperature dataset (`mean=20`, `std=10`, first day Monday),
- computed daily electricity consumption,
- plotted consumption trend over 28 days,
- produced day-of-week average usage bar chart,
- compared weekday vs weekend consumption behavior.

### 2) Modified Iterative Root-Finding Method (20 marks)
I solved:

`f(x) = 2x^2 + 3sin(x) - 4exp(0.5x) + ln(x)`

with iteration:

`x_(k+1) = x_k - f(x_k)/(10f'(x_k)) - f'(x_k)/(600f''(x_k))`

using:
- initial guess `x1 = 2.0`,
- stopping rule `|x_(k+1) - x_k| < 1e-6`.

Deliverables completed:
- root approximation for `f(x)=0`,
- convergence iteration count,
- convergence plot (`|x_(k+1)-x_k|` vs iteration),
- sensitivity analysis with multiple starting values,
- identified non-convergent starting point(s) and discussed failure behavior.

### 3) Rainfall Probability Modelling from Weather Data (40 marks)
I implemented the logistic rainfall probability model:

`P(rain) = 1 / (1 + exp(-(a*tmax + b*tmin + c*af - d*sun)))`

with coefficients:
- `a = 0.05`, `b = 0.04`, `c = 0.03`, `d = 0.02`

using the provided weather dataset.

Deliverables completed:
- calculated average rainfall probability in `2020` for London, Manchester, and Southampton,
- identified the city with highest rainfall probability in `2023`,
- plotted monthly rainfall probability trend for Southampton (`2022`),
- plotted Liverpool annual average rainfall probability (`2020-2023`).

## Repository Contents
- `Python Assgn 1 36638811.ipynb` - Full analysis notebook (submission file)
- `Python Assgn 1 weather_data.csv` - Weather dataset used in Problem 3
- `Python Assignment_1.pdf` - Original assignment brief

## Tools and Libraries
- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Math utilities (`math` / `scipy`-style numerical workflow where needed)

