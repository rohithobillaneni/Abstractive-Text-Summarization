# Abstractive Text Summarization using T5 Model

This Jupyter Notebook (`Abstractive_Text_summarization.ipynb`) contains Python code for abstractive text summarization using the T5 model. It is the task of generating a concise summary that captures the salient ideas of the source text. The generated summaries potentially contain new phrases and sentences that may not appear in the source text.

## Introduction

The T5 model is a transformer-based model developed by Google, capable of performing a wide range of natural language processing tasks, including text summarization. This notebook demonstrates how to fine-tune the T5 model for abstractive text summarization using the CNN/DailyMail dataset.

## Usage

### 1. Installation

Before you run the notebook, please make sure you have the necessary libraries installed. You can install them using the following commands:

```bash
pip install transformers==3.0.0
pip install tensorflow_datasets
pip install rouge_score
pip install gradio
```

### 2. Notebook Content

- **Importing Libraries**: Install and import the required libraries, including transformers, TensorFlow Datasets, Rouge Score, and Gradio.
- **Setting Hyper-Parameters**: Define hyperparameters such as batch size, learning rate, and device (CPU/GPU).
- **Load Dataset and Storing in Files**: Load the CNN/DailyMail dataset and store it in files for training.
- **Load the Basic T5 Model**: Load the T5 model for text summarization.
- **Tokenize Data**: Tokenize the dataset for training and evaluation.
- **Training Model**: Train the T5 model for text summarization using the provided dataset.
- **Calculating Confidence (Rouge Score)**: Evaluate the model's performance using Rouge scores.
- **Loading the Saved Model**: Load the trained model checkpoint for inference.
- **Checking the Model Status**: Check the status of the loaded model, optimizer, and other parameters.
- **Predict the Summary**: Use the loaded model to generate summaries for input text.

### 3. Interface for Input Text and Output Summary

An interactive interface is provided using Gradio, allowing users to input text and obtain the corresponding summary generated by the T5 model.

## Dataset

The code uses the CNN/DailyMail dataset, a widely used benchmark dataset for text summarization tasks. The dataset consists of news articles paired with human-generated summaries.

## Model

The T5 model is loaded from the `t5-small` pretrained model checkpoint. You can fine-tune the model on your own dataset for better performance.

## References

- [Hugging Face Transformers](https://huggingface.co/transformers/)
- [TensorFlow Datasets](https://www.tensorflow.org/datasets)
- [Gradio](https://gradio.app/)
