## Source code for reproducing results

### Overview 📝

This directory contains the Jupyter Notebook used to generate the experimental results, figures, and analyses presented in our paper, "SHARD: A Resource-aware Partitioning Framework for Distributed Inference on Heterogeneous Devices"

The notebook is designed to be a self-contained and executable representation of our methodology. It allows for a complete reproduction of our findings and provides a transparent view of our implementation.


### How to Use 🚀

The notebook can be run in various environments, including locally or on cloud platforms like Google Colab and Kaggle.

#### Environment

  * **Local Execution:** Simply launch a Jupyter session in this directory and open the `.ipynb` file.
  * **Cloud Execution (Google Colab/Kaggle):** The initial cells of the notebook include commands to install the required dependencies in the cloud environment. You can run these first to set everything up.

#### Execution Modes

You can run the notebook in two ways, depending on your goal:

1.  **Step-by-Step Analysis:** For a thorough understanding of our methodology, we recommend running the notebook **cell by cell**. Each cell corresponds to a logical step in our framework (e.g., model profiling, constraint formulation) and is commented to link back to the descriptions in the paper.
2.  **Full Reproduction:** To generate all results and figures from scratch, you can use the **"Run All"** command in Jupyter (`Cell > Run All`).


### Notebook Structure 🔬

The notebook is organized to mirror the workflow described in the paper:

1.  **Setup and Initialization:** Imports necessary libraries and handles environment setup for cloud platforms.
2.  **Model Loading and IR conversion:** Loads the YOLO model and converts it to an ONNX DAG.
3.  **Device and Performance Modeling:** Defines the specifications for the target hardware (GPU, DPU, FPGA), estimates the FLOPs for each node in the computational graph, and calculates the per-node latency and energy estimates.
4.  **Optimization Problem Formulation:** Constructs the Mixed-Integer Linear Programming (MILP) model, defining the objective function and all necessary constraints (precedence, non-overlap, etc.), and the heuristics proposed to solve this optimization problem more efficiently.
5.  **Solving and Analysis:** Executes the solver and our heuristics to find the optimal partitions and analyzes the output.
6.  **Figure Generation:** Contains the code to plot the graphs presented in the evaluation section of the paper.
