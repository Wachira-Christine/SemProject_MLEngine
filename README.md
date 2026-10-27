
# Student Marketplace - Machine Learning Engine

## Project Overview

This project is part of ICS 3202: Artificial Intelligence at Strathmore University.

Our main project focuses on improving trust in student peer-to-peer commerce through a transaction-verified reputation system.

The machine-learning component supports product discovery by predicting how relevant a product is to a student's search query.

## Machine Learning Approach

- Learning type: Supervised Learning
- Task: Multi-class Classification
- Base model: Logistic Regression
- Dataset: Amazon ESCI Shopping Queries Dataset

The model predicts four product-relevance categories:

- E - Exact
- S - Substitute
- C - Complement
- I - Irrelevant

## Dataset Setup

The datasets are not included in this repository because of their large size.

Download the datasets from:

https://github.com/amazon-science/esci-data/tree/main/shopping_queries_dataset

Required files:

1. shopping_queries_dataset_examples.parquet
2. shopping_queries_dataset_products.parquet

Create a folder called `data` inside the project directory and place both files inside it.

## Requirements

Python 3 with the following libraries:

- pandas
- numpy
- matplotlib
- scikit-learn
- pyarrow
- Jupyter

Install the required libraries if they are missing:

```bash
pip install pandas numpy matplotlib scikit-learn pyarrow jupyter
```

## Running the Notebook

1. Open the project folder in VS Code.
2. Open `LogisticRegression_Base.ipynb`.
3. Select a Python kernel.
4. Ensure both datasets are inside the `data` folder.
5. Run the notebook cells in order.

The notebook uses a sample of 1,500 search queries by default to reduce processing time.

## Model Results

Results obtained using the sampled Amazon ESCI dataset:

| Metric | Result |
|---|---|
| Final usable records | 30,297 |
| Training records | 22,171 |
| Testing records | 8,126 |
| Average cross-validation F1 | 0.273 |
| Test accuracy | 35.3% |
| Test macro F1-score | 0.304 |

The model achieved a higher macro F1-score than the majority-class baseline, although its overall classification performance remains limited.

## Future Improvements

- Compare Logistic Regression with other classification algorithms.
- Improve the features used for product matching.
- Test the model using real student marketplace listings.
- Integrate the validated model with the Android marketplace application.

## Project Scope

This machine-learning engine supports product search and discovery. The transaction-verified reputation system is a separate component of the main research project.

