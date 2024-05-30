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

## Setup

To set up this project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/store-sales-analysis.git
