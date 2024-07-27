# Question Answering with SQuAD Dataset
![](https://repository-images.githubusercontent.com/66346289/8b40b380-51c2-11ea-9c2e-7ca809db2132)
This project focuses on building a question-answering system using the SQuAD (Stanford Question Answering Dataset). 
The system uses TF-IDF vectorization and nearest neighbors for document retrieval and leverages the Wikipedia library for querying related information.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Methodology](#methodology)
- [Results](#results)

## Introduction

The goal of this project is to develop a question-answering system that can accurately retrieve and provide answers to questions based on a given context. 
The system uses the SQuAD dataset, which is a benchmark dataset for training and evaluating question-answering models.

## Dataset

The [SQuAD](https://www.kaggle.com/datasets/stanfordu/stanford-question-answering-dataset) dataset contains questions posed by crowdworkers on a set of Wikipedia articles, where the answer to each question is a segment of text from the corresponding reading passage.

- **Train DataFrame Columns:** `id`, `question`, `context`, `answers`, `c_id`
- **Dev DataFrame Columns:** `id`, `question`, `context`, `answers`, `c_id`

## Usage

Run the Jupyter Notebook to train and evaluate the question-answering model:

```bash
jupyter notebook question-answering.ipynb
```

## Project Structure

The project repository contains the following files and directories:

- `question-answering.ipynb`: Jupyter Notebook for training and evaluating the model.
- `README.md`: Project documentation.

## Methodology

1. **Data Loading and Preprocessing**: The dataset is loaded from JSON files and converted into pandas DataFrames. Text preprocessing steps such as tokenization, stop word removal, and lemmatization are performed to clean and prepare the text data for modeling.
2. **Feature Extraction**: The text data is transformed into numerical features using TF-IDF (Term Frequency-Inverse Document Frequency) vectorization. This helps in converting text data into a format suitable for machine learning models.
3. **Document Retrieval**: Nearest neighbors algorithm is used to retrieve relevant documents based on the query.
4. **Answer Extraction**: The extracted documents are used to find the exact answer to the query.
5. **Model Evaluation**: The performance of the model is evaluated using standard metrics like accuracy, Mean Reciprocal Rank (MRR), and top-k accuracy.

## Results

The performance of the model is evaluated on the validation set using the predefined metrics. 
The results demonstrate the effectiveness of using TF-IDF and nearest neighbors for document retrieval in a question-answering system.

- **Mean Reciprocal Rank (MRR)**: 0.5932
- **Top-5 Accuracy**: 0.7160
- **Top-20 Accuracy**: 0.8311
