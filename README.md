# MLOps-Pipeline-for-Screen-Time-Analysis-Using-Apache-Spark-main
MLOps-Pipeline-for-Screen-Time-Analysis-Using-Apache-Spark This project demonstrates a complete MLOps-style pipeline built with Apache Spark for analyzing mobile app screen time. It covers data preprocessing, feature engineering, model training, and model persistence, making it a scalable and production-ready solution for usage prediction.
Objective To predict daily app usage time (Usage (minutes)) based on behavioral data like:

Notifications received

Times app opened

Past usage patterns

Temporal features (day of week, month)

End-to-End Pipeline Stages

Environment & Spark Initialization Installed pyspark and launched a Spark session
Loaded dataset using Spark DataFrame API

Data Cleaning & Feature Engineering Handled null values and duplicates
Parsed and extracted date components (Day of Week, Month)

One-hot encoded categorical variables (App)

Created lag features for Previous_Day_Usage

Engineered interaction feature: Notifications × Times Opened

Feature Vectorization & Scaling Used VectorAssembler to combine features
Applied MinMaxScaler to normalize numerical values

Data Storage Saved the processed dataset in Parquet format for efficient storage and reusability

Model Training: Random Forest Regressor Selected relevant features for prediction

Split dataset into training and testing sets (80/20)

Trained a RandomForestRegressor using Spark MLlib

Evaluated the model using Mean Absolute Error (MAE)

Model Persistence Saved the trained model for future deployment or inference

Results Model: Random Forest Regressor (100 trees)

Evaluation Metric: Mean Absolute Error (MAE)

Outcome: Trained model can accurately predict daily usage minutes based on behavioral signals

Tech Stack Apache Spark (PySpark)

MLlib (Machine Learning in Spark)

Google Colab + Drive (for storage and environment)

Python (Pandas, Matplotlib, Plotly) for lightweight EDA
