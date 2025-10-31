# medical-insurance-charges-prediction

# Medical Cost Personal Dataset - Neural Network Regression

This project demonstrates how to build and train neural networks to predict medical insurance charges using the Medical Cost Personal Dataset from Kaggle.

## Dataset Information

The dataset contains 1338 records with the following features:
- **age**: Age of the primary beneficiary
- **sex**: Gender (male/female)
- **bmi**: Body mass index
- **children**: Number of children covered by health insurance
- **smoker**: Smoking status (yes/no)
- **region**: Residential area in the US (northeast, southeast, southwest, northwest)
- **charges**: Individual medical costs billed by health insurance (target variable)

## Project Structure

The notebook contains the following sections:

### 1. Importing Libraries
- TensorFlow for building neural networks
- Pandas for data manipulation
- Matplotlib and NumPy for visualization and numerical operations
- Scikit-learn for preprocessing and model evaluation

### 2. Data Preprocessing
- One-hot encoding for categorical variables (sex, smoker, region)
- Feature scaling for numerical variables (age, bmi, children) using MinMaxScaler
- Train-test split (80-20 ratio)

### 3. Model Development
Three different neural network architectures were experimented with:

**Base Model:**
- 50 neurons in hidden layer, 1 output neuron
- SGD optimizer, 100 epochs

**Model 1 (Improved):**
- 100 → 10 → 1 layer architecture
- Adam optimizer, 100 epochs

**Model 2:**
- Same architecture as Model 1 but trained for 300 epochs

**Model 3:**
- Same architecture with different metrics and optimizer configuration

### 4. Model Evaluation
Models were evaluated using Mean Absolute Error (MAE):
- Base Model: ~3521 MAE
- Model 1: ~3362 MAE
- Model 2: ~3475 MAE
- Model 3: ~3470 MAE

### 5. Visualization
Training loss curves were plotted to monitor model performance and convergence.

## Files in the Repository
- insurance.csv: The dataset containing medical insurance records with features like age, sex, BMI, smoking status, region, and insurance charges
- A_larger_example.ipynb: Jupyter notebook containing the complete code for data preprocessing, neural network modeling, training, evaluation, and visualization

## Usage

To run this project:
1. Ensure all required libraries are installed
2. The dataset is automatically downloaded from the provided GitHub URL
3. Run the cells sequentially to preprocess data, train models, and evaluate performance


## Potential Improvements

- Hyperparameter tuning
- Feature engineering
- Trying different neural network architectures
- Using regularization techniques to prevent overfitting
- Ensemble methods

## Data Source

The dataset is available on:
- **Kaggle**: https://www.kaggle.com/datasets/mirichoi0218/insurance
- **GitHub**: https://gist.github.com/meperezcuello/82a9f1c1c473d6585e750ad2e3c05a41

The raw CSV file used in `pd.read_csv` is from the GitHub gist.
