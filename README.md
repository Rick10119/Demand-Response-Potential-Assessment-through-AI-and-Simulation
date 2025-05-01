![image](https://github.com/user-attachments/assets/ea565a28-3da8-4291-aca6-43a6d88f39fa)

# DPAAS: A Data-Driven Framework for Assessing Building Demand Response Potential at Scale

This repository contains the code for the paper:

Ruoxu Chen, Zhuofan Tang, Ruike Lyu, Qingrong Zheng, Haotian Song, Hongye Guo*. Combining AI and Simulation to Assess Building Demand Response Potential at Scale. 2025 IEEE 5th International Conference on Advances in Electrical, Electronics and Computing Technology (EECT 2025), Guangzhou, China: IEEE; 2025. (accepted, Best Paper)

## Table of Contents

- [Introduction](#introduction)
- [Data Files](#data-files)
- [Scripts](#scripts)
- [Usage](#usage)
- [Requirements](#requirements)

## Introduction

DPAAS is a framework designed to assess the demand response potential of buildings at scale using data-driven methods. The framework leverages various datasets, including energy consumption data, building metadata, and weather data, to evaluate and predict the demand response capabilities of commercial buildings.


## Data Files

- `comstock_data_columns.csv`: Contains the column names for individual building energy consumption data.
- `comstock_metadata_columns.csv`: Contains the column names for metadata.
- `feature_transformation.xlsx`: Contains mappings for transforming feature values.
- `selected_features_us.xlsx`: Contains the selected feature names with state names of the US dataset.
- `selected_features.xlsx`: Contains the selected feature names.
- `selected_output.xlsx`: Contains the selected output names.

## Scripts

### Data Download

- `download_annual_baseline_and_upgrade_data.ipynb`: Jupyter notebook for downloading annual baseline and upgrade data from ComStock.
- `download_individual_building_profiles.ipynb`: Jupyter notebook for downloading individual building profiles from ComStock.
- `download_data_result.py`: Script for extracting energy consumption data for buildings.

### Data Handling

- `handel_raw_data.py`: Script for constructing datasets from downloaded data, including data cleaning and feature transformation.
- `handel_raw_data_us.py`: Script for constructing datasets from downloaded data for different states, including data cleaning and feature transformation.

### Model Training

- `model_training_basic_nn_feafture_select.py`: Script for training a basic neural network model with feature selection.
- `model_training_other_model_hpp.py`: Script for training other models with hyperparameter tuning.
- `model_training_other_model.py`: Script for training other models.

## Usage

1. **Download Data**: Use the Jupyter notebooks in the `download_annual_baseline_and_upgrade_data.ipynb` and `download_individual_building_profiles.ipynb` to download the necessary data from ComStock.

2. **Prepare Data**: Run the `handel_raw_data.py` or `handel_raw_data_us.py` scripts to prepare the datasets for model training.

3. **Train Models**: Use the scripts in the `model_training_*.py` files to train the models on the prepared datasets.

## Requirements

- Python 3.x
- pandas
- numpy
- scikit-learn
- boto3
- matplotlib
- Jupyter Notebook

Install the required packages using pip:

```sh
pip install pandas numpy scikit-learn boto3 matplotlib jupyter
