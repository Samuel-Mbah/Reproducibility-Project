# Reproducibility-Project
Solver Notebook

Overview

This Jupyter Notebook implements a solver for the puzzle domain using the IDA* algorithm and Bayesian neural networks. The notebook demonstrates the step-by-step process of training a Bayesian neural network to learn and use a heuristic function to solve the puzzle.

Notebook Structure

The notebook is divided into sections:

1. Importing necessary libraries and loading the puzzle data
2. Implementing for example the Puzzle15 class and related functions
3. Implementing the Heuristics class and related functions
4. Implementing the IDAStar class and related functions
5. Implementing the Neural network class and related functions that introduces uncertainty model.
6. Training the Bayesian neural network and evaluating the solver
7. Solving the puzzle using the trained network

Usage

1. Install the required dependencies: numpy, tensorflow, and tensorflow_probability, scipy, torch.
2. Run the notebook cells to train the network and solve the puzzle

Acknowledgements

This implementation is based on the paper "Utilising Bayesian Neural Networks for Solving the 15-Puzzle" by Marom et al. (2020).
