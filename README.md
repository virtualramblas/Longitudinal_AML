# Longitudinal_AML Forecasting

This repository contains the complete codebase, datasets, and analysis workflows for our [paper](https://arxiv.org/abs/2508.13199) "Neurosymbolic Learning for Predicting Cell Fate Decisions from Longitudinal Single-Cell Transcriptomics in Paediatric Acute Myeloid Leukemia". Our complex systems approaches reveal causal drivers of fate plasticity and state-transitions in Pediatric Acute Myeloid Leukemia. Our findings, using deep learning algorithms (Transformer, LSTM) and BDM (Block Decomposition Method) complexity perturbation analysis, reveal core regulatory programs and network instability points that drive AML lineage bias (bifurcations), cell fate plasticity, and metabolic/bioelectric coupling shifts.

The repository includes:

Deep Learning Models: Transformer and LSTM architectures for predictive modeling of AML cell fate dynamics.

Statistical & Regression Models: Bayesian ridge regression for feature importance ranking.

Complexity Analysis: BDM signature extraction, causal perturbation analysis, and network instability mapping.

Bulk RNA-seq Pipeline

Results: Extracted differentially expressed genes (DEGs), feature importance scores, and ranked BDM signatures for reproducibility.

All code and result files are provided to allow full reproduction of the analyses in the manuscript.
Note: In the bulk transcriptome analysis code, please comment out Breast and Pros samples in the final snippet. 
These were additional tissue samples used for comparative analysis.  
## Getting the Raw Data
The bulk Pediatric Leukemia Transcriptome raw data can be downloaded from [here](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE7757). The total size of the compressed data on disk is 7.54 GB. This dataset includes 28 patients data that has been measured at 3 different temporal states: DX (Diagnosis), REL (Relapse), REM (Remission).  
## AML Code Execution
Create a Python virtual environment with your tool of choice, activate it and then install the requirements listed in the ```requirements.txt``` file. MacOS users with Apple Silicon must install also the requirement listed in the ```requirements_mac.txt``` file to use hardware acceleration (recommended for LSTMs and Transformer training in particular). The end-to-end code is included in the ```AML Code.ipynb``` notebook (Jupyter, JupyterLab or VS Code with Jupyter notebook support installed is needed for running it).  
