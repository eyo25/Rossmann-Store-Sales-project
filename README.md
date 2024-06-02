# Rossmann-Store-Sales-project
# Store Sales Analysis

This project analyzes the impact of competitor store openings on the sales of existing stores. The analysis aims to identify how the presence of new competitors affects store performance and provide insights for strategic planning.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Setup](#setup)
- [Analysis](#analysis)
- [Results](#results)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Overview

In this project, we use a dataset containing sales information of different stores, along with details about competitors. We aim to understand how the opening of new competitors influences the sales performance of these stores.

## Dataset

The dataset includes the following files:

- `train.csv`: Contains sales data for training.
- `store.csv`: Contains additional information about the stores.

### Columns in `train.csv`

- `Id`: An ID representing a (Store, Date) tuple.
- `Store`: Unique ID for each store.
- `Sales`: The turnover for any given day (this is what we are predicting).
- `Customers`: The number of customers on a given day.
- `Open`: Indicator for whether the store was open: 0 = closed, 1 = open.
- `StateHoliday`: Indicates a state holiday.
- `SchoolHoliday`: Indicates if the (Store, Date) was affected by the closure of public schools.

### Columns in `store.csv`

- `Store`: Unique ID for each store.
- `StoreType`: Differentiates between 4 different store models: a, b, c, d.
- `Assortment`: Describes an assortment level: a = basic, b = extra, c = extended.
- `CompetitionDistance`: Distance to the nearest competitor store.
- `CompetitionOpenSince[Month/Year]`: The year and month the nearest competitor was opened.
- `Promo`: Indicates whether a store is running a promotion on that day.
- `Promo2`: A continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating.
- `Promo2Since[Year/Week]`: The year and calendar week when the store started participating in Promo2.
- `PromoInterval`: Describes the consecutive intervals Promo2 is started.

- ## Introduction

This project aims to predict daily sales for Rossmann stores using Long Short Term Memory (LSTM) networks. Accurate sales forecasting is crucial for optimizing inventory, staffing, and marketing efforts. The project leverages deep learning techniques to capture temporal dependencies in sales data.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Data Preparation](#data-preparation)
3. [Modeling](#modeling)
4. [Evaluation](#evaluation)
5. [Usage](#usage)
6. [Contributing](#contributing)
7. [License](#license)

## Project Overview

Rossmann operates over 3,000 drug stores across Europe. The task is to predict daily sales for a set of stores. This project uses LSTM, a type of Recurrent Neural Network (RNN), which is particularly suited for time series forecasting.

## Data Preparation

The data preparation steps include:

- **Loading Data:** The dataset is loaded and focused on a single store for simplicity.
- **Stationarity Check:** The Augmented Dickey-Fuller test is used to check for stationarity.
- **Differencing:** If the data is not stationary, differencing is applied to remove trends.
- **Autocorrelation Analysis:** Autocorrelation and partial autocorrelation plots help understand dependencies.
- **Supervised Learning Transformation:** The time series data is transformed into a supervised learning format using a sliding window approach.
- **Scaling:** Data is scaled to the (-1, 1) range for better performance with LSTM.

## Modeling

An LSTM model with two layers is built and trained to predict sales. The model captures long-term dependencies in the sales data. The main steps are:

- **Building the Model:** Construct a sequential LSTM model with two LSTM layers and a Dense output layer.
- **Training the Model:** Train the model on the prepared dataset.
- **Evaluation:** Evaluate the model's performance using metrics like Mean Squared Error (MSE) and visualize predictions.

## Evaluation

The model's performance is evaluated on test data. Evaluation includes:

- **Metrics:** Calculation of Mean Squared Error (MSE) and Mean Absolute Error (MAE).
- **Visualizations:** Plotting predicted sales against actual sales to assess model performance.

## Usage

### Prerequisites

Ensure you have the following installed:

- Python 3.x
- TensorFlow
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Statsmodels

### Running the Project

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/rossmann-store-sales-prediction.git
   cd rossmann-store-sales-prediction

## Setup

To set up this project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/store-sales-analysis.git
