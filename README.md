# LFMC_WildFire_Pred
Predicting Wildfires with Machine Learning  This repository utilizes machine learning to forecast wildfires, a growing concern amid escalating global temperatures. Leveraging live fuel moisture content (LFMC) data obtained through microwave remote sensing.

# Wildfire Prediction using Machine Learning

## Introduction

As we see a rise in the temperature across the globe, its potential to burn has also increased. Over the past few decades, there have been many incidents of occurrence of wildfires in the world. An earlier prediction of forest fires can help in better wildfire risk management.

To predict wildfires, one of the key indicators is live fuel moisture content (LFMC) obtained from ** Google Earth ** , which means the mass of water per unit dry biomass in vegetation. LFMC data is captured at a large scale based on microwave remote sensing and eventually represented as maps.


### Problem Definition: Given the image dataset, determine whether there will be fire in the next 15 days within 8km ∗ 8km grid

## Data and Methodology

We utilized LFMC maps and the ground truth wildfire data from fire.ca.gov to predict whether there will be a fire in the near future within the 8km x 8km grid using machine learning models such as SVM and Random Forest. Problem Definition and Algorithm
The dataset we have are LFMC maps that are downloaded using Google earth engine API and the ground truth wildfire data has been taken from California Department of Forestry and Fire Protection over the same duration

![image](https://github.com/manvendra-nema/LFMC_WildFire_Pred/assets/53614640/5662ab02-edbc-4e8b-bf9e-f5b9433e5397)


## Results

Our results show that Random Forest and SVM achieved the following accuracies:

- Random Forest: 91.69%
- SVM: 80%

Concluding that Random Forest performs better for this wildfire prediction task.

## Repository Contents

- `data/`: Directory containing datasets used in the project.
- `notebooks/`: Jupyter notebooks demonstrating data analysis, model training, and evaluation.
- `models/`: Saved trained models.
- `README.md`: This file providing an overview of the project.

## Usage

To replicate the results or explore further:
1. Clone the repository: `git clone https://github.com/your_username/your_repository.git`
2. Navigate to the project directory: `cd your_repository`
3. Explore the notebooks in the `notebooks/` directory for data analysis and model training.

## Dependencies

- Python 3.x
- scikit-learn
- pandas
- numpy
- matplotlib
- geopandas
- rasterio
- pyproj
- pycrs
- ray
- earthengine-api

Note: Result may change w.r.t report as I modifying this after long period with changed dependency.
