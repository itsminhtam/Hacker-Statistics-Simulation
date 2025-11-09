# Hacker Statistics: A "Random Walk" Simulation

This project is a classic Monte Carlo simulation exercise, often dubbed "Hacker Statistics". The goal is to use repeated random steps (thousands of times) to estimate the probability of a complex outcome that is difficult to calculate theoretically.

## The Scenario: Climbing the Empire State Building

We will simulate a person attempting to climb the Empire State Building. We want to find the **probability of reaching the 60th step (or higher)** after 100 moves (100 steps).

A single "random walk" consists of 100 steps. The entire simulation will run 5,000 "walks" to obtain a reliable statistical result.

## Simulation Rules

Each walk begins at step **0** and follows these rules for each of the 100 steps:

1.  **Roll the Dice:**
    * If it's a **1** or **2**: Go **down 1 step**.
    * If it's a **3**, **4**, or **5**: Go **up 1 step**.
    * If it's a **6**: Roll the dice again and go **up** by the number of steps shown on that second roll.

2.  **The "No Going Back" Rule**:
    * A person can never be below step 0. If at step 0, and the dice roll results in "go down", the person stays at step 0.

3.  **The "Clumsiness" Rule**:
    * On *every* step, there is a **0.1% (0.001)** chance of tripping.
    * If the person trips, their position is immediately reset **back to step 0**.

## Objective

The task is to run the simulation 5,000 times, collect the final position of each walk, and calculate the percentage of walks that ended at step 60 or higher.

## Tech Stack

* **Python 3**
* **NumPy**: For random operations and array calculations.
* **Pandas**: For data analysis and managing the simulation results.
* **Matplotlib**: For visualizing the simulation results (histograms and walk plots).

## How to Run

1.  Install the required libraries:
    ```bash
    pip install numpy pandas matplotlib
    ```
2.  Run the main Jupyter Notebook (`simulation.ipynb`).
3.  The script will output the final probability and display visualizations.
