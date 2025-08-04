# Predictive Maintenance of Industrial Machinery

## Problem Statement
This project addresses the challenge of developing a predictive maintenance model for a fleet of industrial machines. The goal is to anticipate failures before they occur by analyzing sensor data to identify patterns that precede a failure. The solution aims to create a classification model capable of predicting the type of failure (e.g., tool wear, heat dissipation, power failure) based on real-time operational data, thereby enabling proactive maintenance, reducing downtime, and lowering operational costs.

## Proposed Solution
The solution involves leveraging data analytics and machine learning techniques to accurately forecast failure patterns, consisting of the following key components:

- **Data Collection**: Utilized historical sensor data from the Kaggle "Machine Predictive Maintenance Classification" dataset.
- **Data Preprocessing**: Performed cleaning and preprocessing of collected data, including feature engineering.
- **Machine Learning Algorithm**: Implemented a high-accuracy multiclass classification model, specifically a Batched Free Ensemble Classifier, developed using IBM Watsonx.ai Studio.
- **Deployment**: The trained model was deployed as an Online Deployment on IBM Cloud Lite services for real-time predictions.
- **Evaluation**: The model achieved an accuracy of 0.995 in predicting failure types, validated through testing.

## System Approach
The system employs a structured, end-to-end methodology within the IBM Cloud ecosystem.

### System Requirements:
- **Platform**: IBM Cloud (mandatory use of Lite services).
- **Core Service**: IBM Watsonx.ai Studio for model development, training, and deployment.
- **Data**: Operational sensor data from industrial machinery.
- **Problem Type**: Multiclass classification.
- **Deployment**: Real-time "Online" web service.
- **Performance**: High accuracy in failure prediction.

### Libraries Required to Build the Model:
The model was built using the AutoAI feature in IBM Watsonx.ai Studio. This automated process internally utilized algorithms such as Snap Random Forest Classifier and Batched Free Ensemble Classifier.

## Algorithm & Deployment
A robust machine learning algorithm was selected and deployed as a real-time web service.

- **Algorithm Selection**: A Batched Free Ensemble Classifier (a variant of Snap Random Forest Classifier) was chosen due to its high accuracy (0.995) in multiclass classification, automatically identified by AutoAI.
- **Data Input**: The algorithm processes sensor data including:
  - Unique Device Identifier (UDI)
  - Product ID
  - Type (L, M, H)
  - Air temperature [K]
  - Process temperature [K]
  - Rotational speed [rpm]
  - Torque [Nm]
  - Tool wear [min]
- **Training Process**: Automated by IBM Watsonx.ai's AutoAI tool, which handled feature engineering, hyperparameter tuning, and cross-validation across multiple generated pipelines.
- **Prediction Process**: The deployed model accepts real-time operational data inputs and provides instant predictions of failure types along with probability scores.
- **Deployment**: The final model was deployed as an Online Deployment on IBM Cloud Lite services, providing a REST API endpoint for continuous, real-time predictive capabilities.

## Results
The developed system successfully predicts machine failures, enabling proactive maintenance. During testing, the model demonstrated accurate classification of various failure types, such as "No Failure" and "Power Failure," with high confidence. This capability is expected to significantly reduce downtime and operational costs for industrial machinery. The entire solution was built and deployed using IBM Watsonx.ai Studio on IBM Cloud Lite services.

## Future Scope
- **Integration with CMMS**: Integrate the model with a Computerized Maintenance Management System (CMMS) for automated work order generation.
- **Real-time Dashboard**: Develop a dashboard for visualizing sensor data, predictions, and alerts.
- **Prescriptive Maintenance**: Enhance the solution to recommend specific maintenance actions.
- **Continuous Improvement**: Implement a feedback loop for automatic model retraining with new data.

## References
- **Kaggle Dataset**: Shivam. (n.d.). Machine Predictive Maintenance Classification. Retrieved from [Kaggle Dataset](https://www.kaggle.com/datasets/shivamb/machine-predictive-maintenance-classification)
- **IBM Cloud**: IBM. (n.d.). IBM Cloud Lite. Retrieved from [IBM Cloud Lite](https://www.ibm.com/cloud/lite)
- **IBM Watsonx.ai Studio**: IBM. (n.d.). Watsonx.ai Studio. Retrieved from [Watsonx.ai Studio](https://www.ibm.com/products/watsonx-ai)
