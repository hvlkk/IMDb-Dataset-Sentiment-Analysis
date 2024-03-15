# IMDb Dataset Sentiment Analysis

## Table of Contents

- [IMDb Dataset Sentiment Analysis](#imdb-dataset-sentiment-analysis)
  - [Table of Contents](#table-of-contents)
  - [Description](#description)
  - [Project Structure](#project-structure)
    - [Part A: Custom Bernoulli Naive Bayes Implementation](#part-a-custom-bernoulli-naive-bayes-implementation)
    - [Part B: Comparison with Scikit-learn's Bernoulli Naive Bayes](#part-b-comparison-with-scikit-learns-bernoulli-naive-bayes)
    - [Part C: Custom RNN Implementation](#part-c-custom-rnn-implementation)
  - [Installation](#installation)
  - [License](#license)

## Description

This project was developed as part of the second assignment for the Artificial Intelligence class (INF153 - 3531) offered by the Athens University of Economics and Business during the winter semester of 2023-24. It aims to conduct sentiment analysis on the IMDb dataset (also known as "Large Movie Review Dataset"), which can be found in [Stanford&#39;s AI lab](https://ai.stanford.edu/~amaas/data/sentiment/), [Keras](https://keras.io/api/datasets/imdb/) and [Kaggle](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews).

## Project Structure

The project is split into three major parts:

### Part A: Custom Bernoulli Naive Bayes Implementation

For the first part of the project, the data is fetched from Keras and the necessary preprocessing steps are taken. Afterwards, a custom implementation of the multivariate variant of Bernoulli Naive Bayes is developed, making use of logarithmic probabilities. The algorithm's performance is then evaluated using accuracy, precision, recall, and F1-score. Subsequently, the evaluation results are visualised through classification reports, confusion matrix heatmaps, metric tables with precise scores, and learning curves for each metric.

### Part B: Comparison with Scikit-learn's Bernoulli Naive Bayes

For the second part of the project, the Bernoulli Naive Bayes estimator developed during the first part of the project has its performance compared against Scikit-learn's Bernoulli Naive Bayes. Their performances are visualised using classification reports, metric tables for exact scores (including differences between the two algorithms), and learning curves displaying their respective metric scores.

### Part C: Custom RNN Implementation

For the third part of the project, a rudimentary bi-directional RNN with GRU cells and an optional self-attention layer was developed. An instance of the RNN is then initialized, and loss over epochs is calculated and plotted in the form of a curve. Following that, the RNN's performance is evaluated by assessing its accuracy, precision, recall, and F1-score, and the scores are compared against the scores of the custom Bernoulli Naive Bayes algorithm developed in the first part of the project.

## Installation

All the code cells have already been executed, so you can simply browse through `imdb_sentiment_analysis.ipynb` and inspect the code without having to install/execute anything. Regardless, if you would like to install the project and run it anew, you should follow the steps below:

1. Clone the repository to your local machine.
2. Navigate to the project directory.
3. Create and activate a virtual environment using a tool like venv or conda (optional but recommended).
   1. Install pip if it is not installed by default upon the creation of the virtual environment.
4. Ensure the version of Python you are using is compatible with Tensorflow, as it is used throughout this project. As of the time of writing this, Tensorflow only works with Python versions that are >=3.7 and \<3.11. The project has been confirmed to work on Python 3.9.18.
5. Install the required dependencies. Regardless of the Python environment management tool you may have opted to use in step 3, the dependencies should be installed through pip, as many of the dependencies included are unavailable on tools like conda under the specific versions listed. You can install the requirements like so:

   ```bash
   pip install -r requirements.txt
   ```

6. Open `imdb_sentiment_analysis.ipynb` and ensure the first code cell (which contains all the imports that are necessary for the project) executes without issues.
7. You're ready to execute the rest of the code in the notebook.

Be warned that depending on your machine, some code cells (especially the ones in the RNN section of the project) might take a long time to execute, and even more so if you tweak the code and make it more complex (e.g. add more layers to the RNN and/or add more train epochs).

## License

[MIT](https://choosealicense.com/licenses/mit/)
