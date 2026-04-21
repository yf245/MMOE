# Code for 'Monotonic Mixture-of-Experts for Monotonic Regression'

This repository contains the code and datasets used in our paper **"Monotonic Mixture-of-Experts for Monotonic
Regression."**

**Abstract**: Shape constraints, such as monotonicity, arise in many scientific and engineering applications, as motivated by governing physics, underlying theory, or domain knowledge. As such, a growing trend in machine learning (ML) calls for shape-constrained regression models that impose monotonicity constraints. Along these lines, this work is concerned with introducing monotonicity constraints in the context of mixture of experts (MoE) models, which are prevalent ensemble ML methods for efficiently learning from complex and heterogeneous datasets. In the MoE framework, multiple ML models (referred to as experts) are trained on distinct data subsets and then merged to form a mixture using input-dependent weights. We show that achieving monotonicity in MoE models is non-trivial since the resulting mixture is not guaranteed to be monotone even if the constituting experts are. Motivated by that, we propose an MoE method that introduces monotonicity by leveraging a special class of polynomial functions as experts, and then internalizing a constrained optimization that directly acts on their coefficients. Experiments on four real-world case studies in energy and materials sciences show that the proposed approach effectively preserves the monotonicity of the mixture model at a minimal compromise of predictive performance. 

## Getting Started

- **Requirements**: Install Conda (either Miniconda or Anaconda).
- **Installation**: 
	- Open your terminal and navigate to the local folder where you want the project to be in:  `cd /path/to/your/folder`
	- Run the clone command: `git clone https://github.com/yf245/MMOE.git`
	- Change into the cloned directory: `cd MMOE`
	- Create a virtual environment: `conda create -name <venv_name> python=3.9.7`
	- Activate the virtual environment: `conda activate <venv_name>`
	- Install packages in the virtual environment: `conda install --file requirements.txt`
	- Open JupyterLab: `jupyter lab` 
	- Please refer to the next section for usage.
	- When you are done, deactivate the virtual environment: `conda deactivate`

## Usage

To reproduce the figures and the tables in our paper, please run the Jupyter Notebooks depending on the model of interest to you. 

More instructions will be available in the Notebooks to guide you further.

## File Structure

- `requirements.txt`: Lists all the packages you need
- `MMIE_and_Baseline_MoE.ipynb`: Contains all the code you need to generate or reproduce the results for MMIE and Baseline MoE models
- `Proposed_MMoE_and_BP.ipynb`: Contains all the code you need to generate or reproduce the results for proposed MMoE and BP models
- `sensitivity_analysis.ipynb`: Contains all the code you need to generate or reproduce the results for Figures 2b and 2c
- `data/` and `new_datasets/`: Contain the data that will be used by the two Jupyter Notebooks
- `baseline_fitted_models/`: Contains the already fitted Baseline MoE and MMIE models for the turbine dataset, and also save any intermediate outputs
- `proposed_fitted_models/`: Contains the already fitted proposed MMoE model for the turbine dataset, and also save any intermediate outputs