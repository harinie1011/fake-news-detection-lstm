# Fake News Detection Using LSTM

## Overview
This project uses a Long Short-Term Memory (LSTM) neural network to classify news articles as fake or real based on their textual content.

## Technologies Used
- Python
- TensorFlow / Keras
- Pandas and NumPy
- Scikit-learn
- Matplotlib and Seaborn

## Dataset
The project uses a balanced subset of 2,000 articles from the Kaggle Fake and Real News Dataset:
https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset

- 1,000 fake news articles (label 0)
- 1,000 real news articles (label 1)

## Methodology
1. Load the dataset and handle missing values.
2. Clean and preprocess article text.
3. Split the data into training and testing sets.
4. Tokenize the text and pad numerical sequences.
5. Train an LSTM model using TensorFlow/Keras.
6. Evaluate the model and predict labels for unseen text.

## Model Architecture
Embedding → LSTM → Dropout → Dense with Sigmoid

- Optimizer: Adam
- Loss: Binary cross-entropy
- Maximum epochs: 4, with early stopping
- Batch size: 32

## Results

| Metric | Score |
|---|---:|
| Accuracy | 91.25% |
| Precision (Real class) | 87.33% |
| Recall (Real class) | 96.50% |
| F1-score (Real class) | 91.69% |

The model achieved 91.25% accuracy on a held-out test set of 400 articles.

## Limitations
The model learns patterns from its training dataset and does not independently verify the factual accuracy of news. Results may vary on articles from new sources or different topics.

## How to Run
1. Download the dataset from Kaggle.
2. Open the notebook in Google Colab.
3. Upload `Fake.csv` and `True.csv`.
4. Run the notebook cells in order.

## Disclaimer
This is an educational machine learning project. Predictions should not be treated as definitive fact-checks.
