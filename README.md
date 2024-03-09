# IMDb Dataset Sentiment Analysis

## Table of Contents

- [IMDb Dataset Sentiment Analysis](#imdb-dataset-sentiment-analysis)
  - [Table of Contents](#table-of-contents)
  - [Description](#description)
  - [Project Structure](#project-structure)
    - [Part A: Custom Bernoulli Naive Bayes implementation](#part-a-custom-bernoulli-naive-bayes-implementation)
    - [Part B: Comparison with Scikit-learn's Bernoulli Naive Bayes](#part-b-comparison-with-scikit-learns-bernoulli-naive-bayes)
    - [Part C: Custom RNN implementation](#part-c-custom-rnn-implementation)
  - [Installation](#installation)
  - [License](#license)

## Description

This project was developed as part of the second assignment for the Artificial Intelligence class (INF153 - 3531) offered by the Athens University of Economics and Business (AUEB), during the winter semester of 2023-24. It aims to conduct sentiment analysis on the IMDb dataset (also known as "Large Movie Review Dataset"), which can be found in [Stanford's AI lab](https://ai.stanford.edu/~amaas/data/sentiment/), [Keras](https://keras.io/api/datasets/imdb/) and [Kaggle](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews).

## Project Structure

The project is split into three major parts:

### Part A: Custom Bernoulli Naive Bayes implementation

For the first part of the project, the data is fetched from Keras and the necessary preprocessing steps are taken. Afterwards, a custom implementation of the multivariate variant of Bernoulli Naive Bayes is developed, making use of logarithmic probabilities. The algorithm's performance is then evaluated using accuracy, precision, recall, and F1-score. The evaluation results are then visualized through classification reports, confusion matrix heatmaps, metric tables with exact scores, and learning curves for each metric.

### Part B: Comparison with Scikit-learn's Bernoulli Naive Bayes

For the second part of the project, the Bernoulli Naive Bayes estimator developed in the first part has its performance compared against Scikit-learn's Bernoulli Naive Bayes. Their performances are visualized using classification reports, metric tables for exact scores (including differences between the two algorithms), and learning curves displaying their respective metric scores.

### Part C: Custom RNN implementation

For the third part of the project, a rudimentary bi-directional RNN with GRU cells and an optional self-attention layer is developed. Afterwards, loss over epochs is calculated and plotted in the form of a curve. Following that, the RNN's performance is evaluated by assessing its accuracy, precision, recall, and F1-score, and the scores are compared against the scores of the custom Bernoulli Naive Bayes algorithm developed in the first part.

## Installation

All the code cells have already been executed, so one can simply browse through `imdb_sentiment_analysis.ipynb` and inspect the code without having to install/execute anything. Regardless, if you would like to install the project and run it anew, you should follow the steps below:

1. Clone the repository to your local machine.

2. Navigate to the project directory.

3. Create and activate a virtual environment using a tool like venv or conda (optional but recommended). For example, if you opt to use venv; on Windows, you can create a virtual environment named 'env' in the current directory by running `python -m venv env` and then activate it using `.\env\Scripts\activate`. On MacOS/Linux, you can create a virtual environment named 'env' by running `python3 -m venv env` and activate it using `source env/bin/activate`.

4. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

5. Open the notebook file (`imdb_sentiment_analysis.ipynb`) and ensure the first code cell (which contains all the necessary imports) executes without issues.

6. You're ready to execute the rest of the code in the notebook.

Be warned that depending on your machine, some code cells (especially the ones in the RNN part of the project) might take a long time to execute, and even more so if you tweak the code to be more complex (e.g. add more layers to the RNN and/or more train epochs).

## License

[MIT](https://choosealicense.com/licenses/mit/)
