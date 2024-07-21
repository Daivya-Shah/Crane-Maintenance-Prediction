# Crane Maintenance Prediction Using Machine Learning

## Project Overview
This project focuses on predicting whether maintenance is required for cranes based on various operational and environmental factors. The project utilizes a Support Vector Machine (SVM) classifier to analyze the data and make predictions, ensuring efficient and timely maintenance.

## Feature Descriptions and Ranges
- **Crane_ID**: ID for each crane (Range: 1-10)
- **Ambient_Temperature**: Temperature around the crane (Range: 0°C-50°C)
- **Humidity**: Environmental humidity level (Range: 30%-90%)
- **Wind_Speed**: Speed of wind affecting the crane (Range: 0-20 m/s)
- **Operation_Type**: Type of operation, encoded (0 = Loading, 1 = Unloading, 2 = Moving)
- **Operation_Hours**: Hours crane was operational (Range: 0-24 hours)
- **Load_Weight**: Weight handled by the crane (Range: 1-50 tons)
- **Number_of_Lifts**: Lifts performed by the crane (Range: 1-300)
- **Motor_Current**: Current drawn by the crane’s motor (Range: 10-500 Amps)
- **Hydraulic_Pressure**: Hydraulic system pressure (Range: 500-3000 psi)
- **Oil_Level**: Oil level percentage (Range: 0%-100%)
- **Oil_Viscosity**: Hydraulic oil viscosity (Range: 10-1000 centistokes)
- **Average_Daily_Motor_RPM**: Motor RPM (Range: 0-10,000 RPM)
- **Peak_Load_Weight**: Maximum load weight handled (Range: 1-50 tons)
- **Time_Since_Last_Maintenance**: Days since last maintenance (Range: 0-365 days)
- **Crane_Age**: Age of the crane (Range: 0-30 years)
- **Usage_Frequency**: Days per week crane is used (Range: 1-7 days)
- **Number_of_Past_Failures**: Past failures (Range: 0-9)
- **Maintenance_Frequency**: Annual maintenance occurrences (Range: 1-12)

### Maintenance Conditions:
- **Motor Current**: Maintenance needed if >375 Amps.
- **Hydraulic Pressure & Oil Level**: Maintenance needed if pressure >2250 psi and oil level <25%.
- **Crane Age**: Maintenance needed if age >15 years.
- **Past Failures**: Maintenance needed if failures >7.
- **Usage & Maintenance Frequency**: Maintenance needed if usage is daily and frequency <4 times/year.

## Implementation Details

### Data Preprocessing
- Standardized the data to a common range using `StandardScaler`.
- Split the data into training and testing sets using `train_test_split`.

### Model Training
- Used a Support Vector Machine (SVM) classifier with a linear kernel.
- Trained the model on the training data and evaluated its accuracy on both training and testing data.

### Prediction
- Implemented a function to predict whether maintenance is required based on new input data.

## Results
- **Training Data Accuracy**: 83.93%
- **Testing Data Accuracy**: 84.66%
