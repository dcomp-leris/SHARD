## Paper Results 📊

### Overview

This directory contains the primary output file from the experiments described in our paper, "SHARD: Scalable Heterogeneous Assignment for Resource-aware Deployment."

All experimental results, including final partitions, performance metrics, and solver statistics, are consolidated into a single Python pickle file: `yolo11n_solution.pkl`. The plots generated from the data in `yolo11n_solution.pkl`, corresponding to the figures presented in the paper, can be found in the `/plots/` sub-directory. The key figures include:

  * `computing_energy_per_device.pdf`: Compares the energy cost provided by each approach for every device (Figure 3(a) in the paper).
  * `computing_time_per_device.pdf`: Compares the computation time provided by each approach for every device (Figure 3(b) in the paper).
  * `flops_computed_per_device.pdf`: Compares the computational load (in FLOPs) allocated to each device by every approach (Figure 3(c) in the paper).
  * `dag_completion_time.pdf`: Compares the time required to compute all nodes of the DAG on every device for each partitioning strategy (Figure 4 in the paper).
  * `execution_time_of_each_approach.pdf`: Compares the time required by each approach to find a solution (Figure 5 in the paper).

### File Description & Data Structure 🔬

The `yolo11n_solution.pkl` file contains a Python dictionary. This dictionary holds the complete results for the different optimization methods and heuristics evaluated in our study.

You can load and inspect the data in Python as follows:

```python
import pickle

with open("yolo11n_solution.pkl", "rb") as f:
    results = pickle.load(f)

# Example: Access the results for the F1 method
f1_results = results['F1']
print(f1_results)
```

#### Dictionary Keys

The dictionary contains the following keys, corresponding to the different experimental runs:

  * `'F1'`: Results for the **Formal (MILP) Method, 1-Stage Optimization**.
  * `'F2'`: Results for the **Formal (MILP) Method, 2-Stage Optimization**.
  * `'H1'`: Results for the **Heuristic Method 1**.
  * `'H2'`: Results for the **Heuristic Method 2**.

#### Value Structure

For each key, the value is a list containing six elements in the following order:

1.  `objective_value` (float): The final value of the objective function (e.g., total energy).
2.  `makespan` (float): The total end-to-end latency of the pipeline (completion time of the last node).
3.  `start_times` (dict): A dictionary mapping each node index to its scheduled start time.
4.  `end_times` (dict): A dictionary mapping each node index to its scheduled completion time.
5.  `solution` (dict): The final node-to-device partition mapping.
6.  `execution_time` (float): The wall-clock time it took for the method itself to run and produce the solution.

### How to Reproduce 🔄

This result file is generated programmatically. To regenerate it, please run the Jupyter Notebook located in the `../code/` directory, following the instructions in its `README.md` file.
