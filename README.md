# Walking & Running Classification — Motion Sensor ML Model
This project focuses on building an end-to-end machine learning system that classifies whether a user is walking or running using raw motion-sensor data.
The dataset contains accelerometer and gyroscope readings captured from a wearable device.
The project includes data exploration, feature engineering, model building, model comparison, and challenge resolution, all in a single Jupyter Notebook.

# Tech Stack
Programming & Libraries
- Python: Pandas, NumPy, Matplotlib, Scikit-learn
- Machine Learning: Logistic Regression, Random Forest, KNN, SVM, Multi-layer Neural Networks
- Environment: Jupyter Notebook

Core Techniques
- Sensor data preprocessing
- Feature engineering
- Activity segmentation
-Model training & comparison
- Evaluation metrics (Precision, Recall, F1-score, ROC-AUC)

#Data Source

Dataset Link (Provided by Rubixe):
https://d3ilbtxij3aepc.cloudfront.net/projects/CDS-Capstone-Projects/PRCP-1013-WalkRunClass.zip

#Attributes (11 Total)
- date
- time
- username
- wrist
- activity (target variable)
- acceleration_x, acceleration_y, acceleration_z
- gyro_x, gyro_y, gyro_z

# Problem Statement
The goal of this project is to create a predictive machine learning model that accurately classifies whether a user is walking or running based on motion-sensor readings.

# Task Breakdown
- Task 1: Prepare a complete exploratory data analysis (EDA) report.
- Task 2: Build predictive models to classify walking vs running.
- Task 3: Compare models and select the best for production.
- Task 4: Document challenges faced and strategies used.

# Goal of the Project
- To classify human physical activity using wearable sensor data.
- To identify patterns in accelerometer and gyroscope readings.
- To evaluate multiple ML models and recommend the best-performing one.
- To produce actionable insights about movement behavior.

# Solution Approach
## ✔ Step 1: Data Cleaning & Preprocessing
- Removed missing values and inconsistent timestamps
- Merged date/time columns
- Normalized high-variance sensor readings
- Handled sensor noise using smoothing techniques

## ✔ Step 2: Exploratory Data Analysis
- Motion signal behavior visualized over time
- Distribution analysis of acceleration and gyroscope axes
- Activity-based segmentation (walking vs running)

## ✔ Step 3: Feature Engineering
Created new features such as:
- Sensor magnitude (acceleration, gyroscope)
- Rolling averages
- Variability metrics
- Peak detection-based features

## ✔ Step 4: Model Development
- Multi-layer neural networks
- Logistic Regression
- Random Forest
- LSTM Deep Learning Model
- MLP

## ✔ Step 5: Model Evaluation
- Evaluated using:
- Precision
- Recall
- F1 Score
- ROC Curve & AUC Score

# Key Insights & Findings
- Running signals showed higher acceleration and gyroscope variability.
- Neural Networks achieved the highest accuracy due to capturing nonlinear movement patterns.
- Classical models (LR, KNN) performed well but struggled with overlapping boundaries.

# Challenges & Solutions
| Challenge                 | Solution                                                 |
| ------------------------- | -------------------------------------------------------- |
| Sensor noise              | Applied smoothing & normalization                        |
| Class imbalance           | Used stratified train-test split                         |
| High variance in readings | Scaled using StandardScaler                              |
| Overlapping patterns      | Added engineered features like magnitude & rolling stats |
| Missing timestamps        | Interpolation + validation rules                         |

# Impact & Applications
- Wearable device activity recognition
- Fitness tracking apps
- Physiotherapy monitoring
- Real-time gait analysis
- Human motion understanding for AI systems

