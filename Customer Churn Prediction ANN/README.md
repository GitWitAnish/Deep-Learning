# Customer Churn Prediction 

A deep learning project that predicts customer churn using an Artificial Neural Network (ANN) built with TensorFlow/Keras.

## Project Overview

This project implements a binary classification model to predict whether a bank customer will churn (leave the bank) based on various customer attributes. The model uses a feedforward neural network with multiple hidden layers to learn patterns in customer behavior.

## Dataset

The project uses the **Churn_Modelling.csv** dataset containing customer information with the following features:

- **RowNumber**: Row index
- **CustomerId**: Unique customer identifier
- **Surname**: Customer surname
- **CreditScore**: Credit score of the customer
- **Geography**: Customer's country (France, Spain, Germany)
- **Gender**: Customer's gender (Male, Female)
- **Age**: Customer's age
- **Tenure**: Number of years with the bank
- **Balance**: Account balance
- **NumOfProducts**: Number of bank products used
- **HasCrCard**: Whether customer has a credit card (1 = Yes, 0 = No)
- **IsActiveMember**: Whether customer is an active member (1 = Yes, 0 = No)
- **EstimatedSalary**: Estimated salary
- **Exited**: Target variable - whether customer churned (1 = Yes, 0 = No)

## Project Structure

```
Customer Churn Prediction ANN/
│
├── dataset/
│   └── Churn_Modelling.csv      # Raw dataset
│
├── notebook/
│   └── main.ipynb                # Main Jupyter notebook with complete workflow
│
└── README.md                     # Project documentation
```

## Workflow

1. **Data Loading**: Import the customer churn dataset
2. **Data Preprocessing**:
   - Remove unnecessary columns (RowNumber, CustomerId, Surname)
   - One-hot encode categorical variables (Geography, Gender)
3. **Data Splitting**: Split data into training (80%) and testing (20%) sets
4. **Feature Scaling**: Standardize features using StandardScaler
5. **Model Building**: Create a Sequential ANN with:
   - Input layer: 11 neurons (matching feature count)
   - Hidden layer: 11 neurons with ReLU activation
   - Output layer: 1 neuron with Sigmoid activation (binary classification)
6. **Model Training**: Train with Adam optimizer and binary cross-entropy loss
7. **Evaluation**: Assess model performance on test data

## Model Architecture

```
Layer 1 (Input):  11 neurons, ReLU activation
Layer 2 (Hidden): 11 neurons, ReLU activation  
Layer 3 (Output): 1 neuron, Sigmoid activation
```

- **Optimizer**: Adam
- **Loss Function**: Binary Crossentropy
- **Metrics**: Accuracy
- **Batch Size**: 50
- **Epochs**: 100
- **Validation Split**: 20% of training data

