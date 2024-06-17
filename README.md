# Reproducibility-Project

# Training a Neural Network to Solve the 15-Puzzle with IDA* Search

This repository explores training a neural network to act as a heuristic function for the IDA* (Iterative Deepening A*) search algorithm in solving the 15-puzzle. The learned heuristic guides the search process towards the goal state.

## Project Overview

### Environment
- The environment is a 4x4 grid representing the 15-puzzle.
- The `Puzzle15` class defines functionalities like state validation, move generation, cost calculation, and state encoding for neural network processing.

### Tasks
- Tasks with increasing difficulty (number of moves to solve) are generated using the `generate_task_prac` function.

### Algorithm
The `learn_heuristic_prac` function iteratively trains the neural network:
1. Generates tasks and attempts to solve them with IDA* using the current model.
2. If solved, corresponding state-action pairs are added to a memory buffer.
3. The memory buffer is used to train the neural network model.
4. An exploration parameter is adjusted based on the success rate to balance exploration and exploitation.

### Neural Network
Two architectures are available:
1. Simple feed-forward neural network with one hidden layer (FFNN).
2. Weighted Universal Neural Network (WUNN) predicting cost distribution mean and log variance.

### Evaluation
- The primary measure is the success rate of IDA* with the learned heuristic (percentage of solved tasks per iteration).

## Running the Experiments

### Requirements
- Python 3.x
- TensorFlow
- NumPy

### Instructions
1. Clone this repository:
    ```bash
   [git clone https://github.com/Samuel-Mbah/Reproducibility-Project.git]
    cd 15-puzzle-heuristics
    ```

2. Create a virtual environment (optional but recommended):
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```

4. Open the Jupyter Notebook and follow the steps to run the implementation and reproduce the experiments:
    ```bash
    jupyter notebook 15_puzzle.ipynb
    ```
5. Follow the same steps as above for the 24 puzzle domain
### Configuration
Configure training parameters in the code as needed. Key parameters include the number of iterations, tasks per iteration, exploration parameters, and neural network architecture.

## Implementation Details

### Imports and Dependencies
Ensure all necessary libraries are imported at the beginning of the notebook.

### Utility Functions
Define utility functions such as puzzle generation, solving the puzzle, and heuristic learning.

### Parameters and Hyperparameters
Define all necessary parameters and hyperparameters for training and evaluation.

### Model Training
Train the heuristic model based on the provided parameters.

### Evaluation and Analysis
Evaluate the trained model on test data and analyze the results.

## Results
Our experiments aimed to reproduce the results presented in the paper ["Utilising Uncertainty for Efficient Learning of Likely-Admissible Heuristics"](https://www.raillab.org/publication/marom-2020-utilising/marom-2020-utilising.pdf). Despite rigorous efforts and multiple trials, we were unable to replicate the results as reported. Below is a detailed summary of our findings:

- **Implementation Success**:
  - Successfully implemented the `GenerateTaskPrac` algorithm for task generation.
  - Seamlessly integrated the IDA* algorithm for heuristic search.

- **Challenges Encountered**:
  - The `LearnHeuristicsPrac` algorithm did not converge, resulting in a continuous run without producing the expected results.
  - Significant difficulty in implementing the `LearnHeuristicsPrac` algorithm due to the complexity of integrating aleatoric and epistemic uncertainties within the neural network.

- **Hardware and Computational Resources**:
  - Experiments were conducted on an Intel i5-12450H 2.00GHz CPU with 32GB RAM.
  - Initial training for the 15-puzzle took approximately 12 hours but did not yield positive results. Subsequent trials averaged around 8 hours each with similar outcomes.

- **Evaluation Measures**:
  - Despite using the parameters and methodology described in the paper, our implementation did not produce results that supported the main claims of the original study.

### Key Metrics

- **Generated Nodes**: Unable to achieve meaningful results due to non-convergence.
- **Planning Time**: Not applicable due to the lack of convergence.
- **Suboptimality**: Not applicable due to the lack of convergence.
- **Optimal Solved Percentage**: Unable to determine due to non-convergence.

### Strengths and Weaknesses

- **Strengths**:
  - Successful implementation of the task generation algorithm.
  - Effective integration of the IDA* search algorithm.

- **Weaknesses**:
  - Challenges in re-implementing the learning algorithm in Python from the provided C# code.
  - Computational constraints and extensive training requirements that may necessitate more powerful hardware or optimized implementation.

### Conclusion

Our efforts to reproduce the results of the original paper were met with significant challenges, particularly with the `LearnHeuristicsPrac` algorithm. Despite thorough attempts to follow the provided methodology, we were unable to support the claims made in the original study based on our findings.


## References
- [Original Paper](https://www.raillab.org/publication/marom-2020-utilising/marom-2020-utilising.pdf)
- [Supplementary Material](https://www.raillab.org/publication/marom-2020-utilising/marom-2020-utilising_supp.pdf)



## Contact
For any questions or collaboration requests, please contact smwmbah@gmail.com(mailto:smwmbah@gmail.com).
