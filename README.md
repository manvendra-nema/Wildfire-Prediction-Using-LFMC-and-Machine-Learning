# 🔥 FMC WildFire Prediction

## 🌟 Introduction
As we see a rise in the temperature across the globe, its potential to burn has also increased. Over the past few decades, there have been many incidents of occurrence of wildfires in the world. An earlier prediction of forest fires can help in better wildfire risk management.

To predict wildfires, one of the key indicators is live fuel moisture content (LFMC), which means the mass of water per unit dry biomass in vegetation. LFMC data is captured at a large scale based on microwave remote sensing and eventually represented as maps. Using LFMC maps and the ground truth wildfire data from fire.ca.gov, we predicted whether there will be a fire in the near future within the 8km x 8km grid using machine learning models such as SVM and Random Forest. Our results show that Random Forest and SVM gave an accuracy of 91.69% and 80% respectively, concluding that Random Forest performs better.

## 📝 Problem Definition
Given the image dataset, determine whether there will be fire in the next 15 days within an 8km x 8km grid.

## 📊 Data and Methodology

### Data Collection
The dataset we used includes LFMC maps downloaded using the Google Earth Engine API and the ground truth wildfire data from the California Department of Forestry and Fire Protection over the same duration.

### Data Preprocessing
To achieve the task of predicting wildfires using LFMC maps, the dataset required preprocessing. The LFMC maps were .tif files of 250m resolution (i.e., 1 pixel = 250m) of the California region and were generated using Google Earth. The wildfire ground truth data included the date of fire and location coordinates generated using Google Maps and were created as .shp files. We converted the Google Maps location points to Google Earth points to plot the fire points on the LFMC maps.

From the dataset, the nearest previous date from a fire occurring date LFMC map was selected to plot the fire points. A grid of 8km x 8km with the fire point as mid-point (32 x 32 pixels) was cropped. Using this method, we filtered out the fire points for the entire duration. For no fire, we randomly sampled data to extract an image within an 8 months span of the fire occurrence date. The final dataset contains 1928 fire samples and 1928 no fire samples. For machine learning models, the data was split into 80% training set and 20% testing set.

### Machine Learning Models
We experimented with SVM and Random Forest machine learning algorithms for our analysis.

#### SVM (Support Vector Machine)
In machine learning, SVMs are supervised learning models with associated learning algorithms that analyze data for classification. SVMs efficiently perform non-linear classification by implicitly mapping their inputs into high-dimensional feature spaces.

#### Random Forest
Random forests are an ensemble learning method for classification and regression that operate by constructing multiple decision trees at training time. For classification tasks, the output of the random forest is the class selected by most trees.

## 📈 Results
Our results show that:
- **Random Forest:** 91.69% accuracy
- **SVM:** 80% accuracy

Concluding that Random Forest performs better for this wildfire prediction task.

## 🚀 Usage
To replicate the results or explore further:

1. **Clone the repository:**
   ```sh
   git clone https://github.com/your_username/your_repository.git
   cd your_repository
2. **Explore the notebooks:**
Check the notebooks in the notebooks/ directory for data analysis and model training.

## 📦 Dependencies
Python 3.x
scikit-learn
pandas
numpy
matplotlib
geopandas
rasterio
pyproj
pycrs
ray
earthengine-api
Note: Results may change w.r.t the report as I am modifying this after a long period with changed dependencies.
