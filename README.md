# Pheno Predictor

**Pheno Predictor** is a machine learning-based tool designed to predict phenotypic traits (e.g., SNP-related pooled values) from genetic data, specifically using allele sequences. The project utilizes a **Random Forest model** for predictions and applies **CountVectorizer** for transforming allele sequences into k-mers, which can be fed into the model for learning and prediction.

The system predicts phenotypic traits from genotypic data, specifically allele sequences, improving our understanding of genetic effects on wheat traits and advancing agricultural research.

Link to the project: [https://wheat-trait-pro-7d48.onrender.com](https://wheat-trait-pro-7d48.onrender.com)

## Features

- **Random Forest Model**: Utilizes a Random Forest Regressor for predicting SNP-related traits.
- **K-mer Feature Extraction**: Uses **CountVectorizer** to convert allele sequences into k-mers (n-grams) for better model performance.
- **Prediction for Multiple Traits**: Predicts a variety of SNP-related pooled values, such as DH_Pooled, GFD_Pooled, and others.
- **Save and Load Models**: Save trained models and expected column names to disk for later use. Easily load them for making predictions on new data.

## Dataset

The dataset used in this project consists of:
- **Allele Sequences**: DNA sequences represented as strings (e.g., AATTGGCCCCAATTGG).
- **Pooled Values**: A variety of SNP-related metrics (e.g., DH_Pooled, GFD_Pooled, PH_Pooled, etc.), which are the target values predicted by the model.

### Data Format

The dataset must be in CSV format and contain at least the following columns:
- `Allele_Sequence`: A column with the allele sequence strings.
- `DH_Pooled`, `GFD_Pooled`, `GNPS_Pooled`, `GWPS_Pooled`, `PH_Pooled`, `GY_Pooled`: Numeric columns representing the target phenotypic traits to predict.

## Installation

1. Clone the repository to your local machine:
    ```bash
    git clone https://github.com/your_username/pheno-predictor.git
    cd pheno-predictor
    ```

2. Install the required dependencies:
    ```bash
    pip install pandas joblib scikit-learn
    ```

3. Ensure you have the **dataset** in CSV format ready for training and prediction.

## Usage

### Training the Model

To train the model, you need to:
1. Provide the path to your dataset in CSV format.
2. Run the training script, which will:
   - Split the data into training and test sets.
   - Extract features from the allele sequences using **CountVectorizer** (k-mer transformation).
   - Train the **Random Forest Regressor** on the data.
   - Save the model and expected columns to disk.

### Making Predictions

Once the model is trained, you can use the prediction function to make predictions on new allele sequences. The model will predict SNP-related traits (e.g., DH_Pooled, GFD_Pooled) based on input allele sequences.

## Contributing

Contributions to the **Pheno Predictor** project are welcome! If you have any improvements, bug fixes, or suggestions, feel free to fork the repository, create a new branch, and submit a pull request. Please make sure to follow the coding conventions and write tests for any new features.
