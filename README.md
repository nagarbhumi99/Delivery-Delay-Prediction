# Delivery Delay Prediction

## Project Overview
This project analyzes delivery-logistics data to understand the factors associated with delayed deliveries and builds machine-learning classification models to predict whether a delivery will be delayed.

The analysis is performed in Python using a Jupyter Notebook. A Power BI report (`project -2.pbix`) is also included in the project files.

## Objectives
- Explore the percentage of delayed and non-delayed deliveries.
- Investigate delivery delays by weather condition, region, and vehicle type.
- Examine the relationship between delivery distance and delay.
- Prepare numerical and categorical features for machine learning.
- Train and evaluate classification models.
- Predict the delay status for a new delivery record.

## Dataset
The notebook loads a file named `Delivery_Logistics.csv`.

The analysis uses fields such as:
- `delayed` — target variable
- `distance_km`
- `weather_condition`
- `traffic_level`
- `delivery_rating`
- `delivery_cost`
- `package_type`
- `region`
- `vehicle_type`
- `expected_time_hours`
- `delivery_mode`
- `package_weight_kg`
- `delivery_partner`

The notebook removes `delivery_time_hours`, `delivery_status`, and `delivery_id` during preparation. Make sure you have permission to use and share the dataset before publishing it.

## Tools and Libraries
- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Power BI

## Workflow
1. **Load data:** Read the delivery-logistics CSV file.
2. **Inspect and clean:** Review data types, missing values, and duplicate records; prepare selected columns.
3. **Exploratory data analysis:** Visualize delay counts and compare delays across weather conditions, regions, and vehicle types. Examine distance distributions and numerical correlations.
4. **Prepare features:** Separate the target (`delayed`) from the input features and split the data into training and test sets.
5. **Preprocess data:** Impute missing numerical values with the median, scale numerical features, impute missing categorical values with the most frequent value, and one-hot encode categorical features.
6. **Train models:** Evaluate Logistic Regression, Decision Tree, Random Forest, and K-Nearest Neighbors (KNN).
7. **Evaluate:** Compare accuracy and cross-validation scores. The notebook also calculates precision, recall, F1-score, a classification report, and a confusion matrix for Logistic Regression.
8. **Make a prediction:** Run the trained Logistic Regression pipeline on a sample delivery record and inspect prediction errors.

## How to Run
1. Clone or download this repository.
2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```
3. Place `Delivery_Logistics.csv` in a suitable local folder.
4. Open `project-2.ipynb` in Jupyter Notebook.
5. Update the CSV path in the notebook to match your computer, for example:
   ```python
   data = pd.read_csv("Delivery_Logistics.csv")
   ```
6. Run the notebook cells in order.

## Project Files
- `project-2.ipynb` — data analysis, preprocessing, model training, and evaluation.
- `project -2.pbix` — Power BI report file.
- `Delivery_Logistics.csv` — input dataset (include it only if you are allowed to share it).

## Output
The notebook produces exploratory charts, model evaluation metrics, a confusion-matrix heatmap, a model comparison table, and a sample delivery-delay prediction. Actual scores depend on the dataset and execution environment.

## Notes
- The notebook currently contains a local Windows file path for the CSV. Update it before running the project on another computer.
- The notebook uses a sample delivery record for prediction; change its feature values to test other scenarios.
- Review the notebook's preprocessing and evaluation cells before relying on the reported model scores.

## Author
**Bhumi Nagar**
