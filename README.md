# Official PyTorch Implementation of "Purifying Quantization-conditioned Backdoors via Layer-wise Activation Correction with Distribution Approximation" (ICML 2024)

## Overview

This repository contains the official PyTorch implementation required to replicate the primary results presented in the paper "Purifying Quantization-conditioned Backdoors via Layer-wise Activation Correction with Distribution Approximation" for ICML 2024.

## Setup Instructions

This section provides a detailed guide to prepare the environment and execute the LAC project. Please adhere to the steps outlined below.

### 1. Environment Setup

   - **Create a Conda Environment:**  
     Generate a new Conda environment named `lac` using Python 3.8:
     ```bash
     conda create --name lac python=3.8
     ```

   - **Activate the Environment:**  
     Activate the newly created environment:
     ```bash
     conda activate lac
     ```

### 2. Installation of Dependencies

   - **Project Installation:**  
     Navigate to the project's root directory and install it:
     ```bash
     python setup.py install
     ```

   - **Additional Requirements:**  
     Install further required Python packages:
     ```bash
     pip install -r requirements.txt
     ```

## Execution Guidelines

### 1. Prepare the Environment

   - **Navigate to the Project Directory:**  
     Switch to the `main` folder:
     ```bash
     cd ours/main
     ```

   - **Checkpoint Placement:**  
     Download the full-precision model checkpoints (implanted with quantization-conditioned backdoors) from https://www.dropbox.com/scl/fo/pu3ja0djliie0pv70l3b2/h?rlkey=rg1op468jme1lrn7bjnkg06tf&dl=0. 
     Ensure the checkpoint file is stored correctly:
     ```
     ours/main/setting/checkpoint_malicious/pq_cifar_ckpt.pth
     ```

### 2. Run the Project

   - **Execute the Script:**  
     Start the LAC script with the designated template and task:
     ```bash
     python lac.py template=pq_cifar_fp task_name=test pda=True
     ```

## Acknowledgments

The implementation is heavily based on the MQBench framework, accessible at [MQBench Repository](https://github.com/ModelTC/MQBench).

## Citation

Should this work assist your research, feel free to cite us via:

```
@inproceedings{li2024purifying,
title={Purifying Quantization-conditioned Backdoors via Layer-wise Activation Correction with Distribution Approximation},
author={Li, Boheng and Cai, Yishuo and Cai, Jisong and Li, Yiming and Qiu, Han and Wang, Run and Zhang, Tianwei},
booktitle={Forty-first International Conference on Machine Learning},
year={2024}
}
```