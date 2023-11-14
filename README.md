# IMDb Sentiment Analysis with TensorFlow

This project utilizes TensorFlow to perform sentiment analysis on the IMDb dataset, which consists of movie reviews labeled with positive or negative sentiments.

## Overview

The goal of this project is to build a deep learning model using recurrent neural networks (RNNs) to classify movie reviews as either positive or negative based on their text content.

## Dataset

The IMDb dataset is used for training and testing the sentiment analysis model. It is loaded using the TensorFlow IMDb API, and the reviews are converted from integer sequences to text for better understanding.

## Preprocessing

Text data is preprocessed by tokenizing and padding sequences. The Tokenizer class from Keras is employed to convert text to sequences, and the sequences are padded to ensure uniform length for input to the model.

## Model Architecture

The sentiment analysis model is built using a sequential architecture with the following layers:

- Embedding Layer: Converts integer-encoded words into dense vectors of fixed size.
- Dropout Layer: Reduces overfitting by randomly setting a fraction of input units to zero during training.
- Bidirectional LSTM Layers: Captures contextual information in both forward and backward directions.
- Dense Layers: Fully connected layers with ReLU activation for learning complex representations.
- Output Layer: Sigmoid activation for binary sentiment classification.

Additional features include increased embedding dimensions, LSTM units, dropout rates, and a larger dense layer to enhance model complexity.

## Training

The model is trained using the Adam optimizer with gradient clipping. Early stopping is implemented to prevent overfitting, and the training progress is monitored using accuracy and loss metrics.

### Training Results

- Epochs: 8 (early stopping after 8 epochs)
- Training Accuracy: ~97.86%
- Validation Accuracy: ~86.28%

## Evaluation

The model is evaluated on a separate test set, and the accuracy is reported. The results demonstrate the effectiveness of the sentiment analysis model on the IMDb dataset.

### Evaluation Results (Test Set)

- Test Accuracy: ~83.22%

## Usage

To run the code:

1. Clone the repository: `git clone https://github.com/your-username/your-repository.git`
2. Navigate to the project directory: `cd your-repository`
3. Open and run the Jupyter notebook or Python script.

## Dependencies

- TensorFlow
- NumPy
- IMDb dataset
