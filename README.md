# Prediction_commodity_prices

This repository contains a machine learning project aimed at predicting commodity prices, including high-frequency (5-minute interval), mid-frequency (30-minute interval), and daily data. The project leverages various machine learning models to forecast commodity prices based on historical data, and also incorporates sentiment analysis to enhance predictive accuracy.

## Project Overview

The goal of this project is to develop predictive models that can forecast commodity prices using different data frequencies and sentiment analysis. Accurate price predictions are crucial for stakeholders in financial markets, including investors, traders, and companies involved in commodities.

### Key Features:
- **High-frequency prediction:** Analyze and predict prices based on 5-minute and 30-minute intervals.
- **Daily prediction:** Forecast daily commodity prices.
- **Sentiment Analysis:** Incorporate market sentiment data to refine price predictions.
- **Multiple Machine Learning Models:** Includes Linear Regression, Random Forest, and more.
- **Model Evaluation:** Compare models using metrics like MSE, MAPE and R-squared.
- **Calculate the Hurst Exponent (HE) and Local Lyapunov Exponent (LLE)**: Provide insight into the predictability and chaotic nature of the time series data.

## Repository Structure

- `commodities_5mnFF.csv`: Dataset containing commodity prices with a 5-minute frequency.
- `commodities_DAILY.csv`: Dataset containing daily commodity prices.
- `commodity30min.ipynb`: Jupyter notebook for analysis and prediction using 30-minute interval data.
- `commodity5min.ipynb`: Jupyter notebook for analysis and prediction using 5-minute interval data.
- `daily-commodity.ipynb`: Jupyter notebook for analysis and prediction daily data with and without sentimental data.
- `file30.csv`: Dataset containing commodity prices with a 30-minute frequency.

## Getting Started


### Prerequisites

- Python 3.8 or higher
- Jupyter Notebook

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/Prediction_commodity_prices.git
    cd Prediction_commodity_prices
    ```

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

### Usage

1. Open the Jupyter notebooks in the repository using Jupyter Notebook or Jupyter Lab:
    ```bash
    jupyter notebook
    ```

2. Navigate to the desired notebook (`commodity30min.ipynb`, `commodity5min.ipynb`, or `daily-commodity.ipynb`) and run the cells to perform data analysis and model training.

## Methodology

### Data Preprocessing
- **Cleaning:** Handling missing values and outliers.
- **Feature Engineering:** Creating new features based on the existing data to enhance model performance.
- **Normalization:** Scaling the data to ensure all features contribute equally to the model.

### Model Selection
A variety of machine learning models were employed in this project to capture the diverse patterns in commodity price data. The following models were used:
- **Random Forest (RF):** An ensemble learning method that builds multiple decision trees and merges them to obtain a more accurate and stable prediction.
- **Long Short-Term Memory (LSTM):** A type of recurrent neural network (RNN) that is well-suited for sequential data, such as time series. It can learn long-term dependencies, making it ideal for capturing patterns in historical price data.
- **Deep Neural Network (DNN):** A multi-layered neural network that can model complex relationships in the data. The depth of the network allows it to capture a wide range of features.
- **Gradient Boosting Regressor (GBR):** An ensemble learning technique that builds models sequentially, each correcting the errors of its predecessor. It is particularly effective for tabular data with a mix of categorical and continuous features.
- **Linear Regression (LR):** A basic linear approach to modeling the relationship between a dependent variable and one or more independent variables. It serves as a benchmark model in this project.

### Model Evaluation
- **Metrics:** The models are evaluated using MSE (Mean Squared Error) and R-squared to determine their accuracy and goodness of fit.
- **Cross-validation:** Employed to ensure models generalize well on unseen data.

## Prediction Sentiment Price

### Overview
In addition to traditional machine learning models, this project also integrates sentiment analysis to enhance price prediction accuracy. Sentiment analysis involves evaluating market sentiment from various sources, such as news articles, and social media, to determine the overall market mood (positive, negative, or neutral). This sentiment data is then used as an additional feature in the predictive models.

### Methodology
- **Sentiment Data Collection:** Gathered from APIs, google news, and social media platform (Reddit).
- **Sentiment Analysis Techniques:** Natural Language Processing (NLP) techniques like RoBERTa, VADER or TextBlob are used to quantify sentiment.
- **Integration with Models:** Sentiment scores are included as features in the models, to capture the influence of market sentiment on price movements.

## Hurst Exponent (HE) and Local Lyapunov Exponent (LLE) Analysis

### Overview
This project also calculates the Hurst Exponent (HE) and Local Lyapunov Exponent (LLE) for different commodities. These metrics provide insight into the predictability and chaotic nature of the time series data.

- **Hurst Exponent (HE):** Indicates the tendency of a time series to either regress to the mean or cluster in a specific direction. A value of 0.5 suggests a random walk, values less than 0.5 suggest mean reversion, and values greater than 0.5 suggest a trend.
- **Local Lyapunov Exponent (LLE):** Measures the rate of separation of infinitesimally close trajectories in the time series. It helps to assess the chaotic behavior of the system, with higher values indicating more chaotic dynamics.


## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or additions.

