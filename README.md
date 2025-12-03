# Capstone Project (EDA) – Stellar Classification

This project explores the Kaggle Star Dataset, which contains physical properties of different types of stars. The goal is to perform exploratory data analysis (EDA) and build a baseline machine learning model (a second one was added for comparison) to predict the star type.

## Dataset

The dataset includes 240 stars with the following features:

- Temperature (K)
- Luminosity (L/Lo)
- Radius (R/Ro)
- Absolute Magnitude (Mv)
- Star Color
- Spectral Class
- Star Type (target)

## Part 1: EDA

The EDA focused on understanding the dataset structure, feature distributions, and relationships between variables. The following steps were completed:

- Checked data types and summary statistics
- Verified that there were no missing values or duplicates
- Examined the distribution of the star type classes
- Created histograms for the numerical features
- Reviewed the counts of the categorical variables
- Created a scatter plot of temperature vs luminosity

The dataset was already clean and only required encoding of the categorical variables before modeling.

## Part 2: Machine Learning Models

Two models were built (Decision Tree and KNN).

### Decision Tree Classifier

Categorical variables were one-hot encoded manually. The dataset was split into training and testing sets using an 80/20 stratified split. A DecisionTreeClassifier was then trained. The model reached perfect accuracy on the test set, which is expected because the classes in this dataset are strongly separable.

### K-Nearest Neighbors (KNN) Classifier

The same encoded dataset was used. Since KNN is sensitive to the scale of numerical features, the numeric columns were standardized using StandardScaler. The model was trained using k=5. KNN model did not reach perfect accuracy, however, it still performed well. 

## Results

Both models performed well, however, Decision Tree reached perfect accuracy, which makes it superior to the KNN for this problem. 
