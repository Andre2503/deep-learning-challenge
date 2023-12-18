# deep-learning-challenge

# Alphabet Soup Charity Success Prediction

## Overview
- **Objective**: Develop a deep learning binary classifier to predict applicant success for Alphabet Soup's funding.
- **Method**: A neural network model was trained to differentiate between successful and unsuccessful funding applications.

## Repo Structure
- `Starter_Code.ipynb`: Jupyter notebook containing dataset pre-processing and initial model setup.
- `AlphabetSoupCharity_Optimization.ipynb`: Notebook with different dataset pre-processing and various attempts to improve the model.

## Results

### Data Pre-processing
- **Target Variable**: `IS_SUCCESSFUL` (1 = Yes, 0 = No) - indicates whether the recipient used the funds effectively.
- **Features Utilized**:
  - Application type
  - Sector of industry affiliation
  - Government organization classification
  - Funding use case
  - Organization type
  - Active status
  - Income classification
  - Special considerations for the application
  - Requested funding amount
- **Excluded Features**: Attributes like ID number and organization name were omitted from the input data, as they are non-predictive.
- **Feature Binning**: Categories with fewer instances in "application types" and "government organization classification" were aggregated into an 'other' category.

### Model Architecture and Performance
- **Initial Structure**: The neural network starts with an input layer of 16 neurons for 44 input features, followed by a hidden layer of 16 neurons. Both layers use ReLU activation functions, and the output layer uses a sigmoid function for binary classification.
- **Rationale**: The model configuration was based on educational exercises and best practices.
- **Performance Metrics**: The model sought to achieve an accuracy of 0.75 but reached a maximum of 0.7244 on test data.

## Challenges and Improvements
- **Classification Complexity**: The model's learning may be impacted by the reduction from 45 classification types and 17 application categories to simpler forms.
- **Parameter Tuning**: Despite using various parameters to enhance model accuracy, the highest accuracy achieved was 0.7268, using Keras Tuner for hyperparameter optimization.

## Suggestions for Model Improvement
- **Hyperparameter Optimization**: Utilize optimization techniques like grid search or random search to find the best combination of hyperparameters.
- **Regularization Techniques**: Integrate dropout layers or L1/L2 regularization to mitigate overfitting.
- **Feature Engineering**: Reassess and possibly enhance the feature set to ensure all features are relevant and potentially introduce new features that better capture application success.
