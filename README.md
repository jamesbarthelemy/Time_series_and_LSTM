# Long Short-Term Memory Neural Network for Financial Time Series

Nowadays, the emergence of Machine Learning and more recently Deep Learning has brought a new dimension to the theory of time series. Indeed, Deep learning methods offer many promises for time series forecasting, such as the automatic learning of time dependence and automatic management of time structures (trends and seasonality).

In this project, implementing the attached arXiv paper, I will present to you the different avenues explored concerning the development of a prototype using a recurrent neural network LSTM for the prediction of the evolution of stock prices. 

# Table of contents

1. [Problem description](#problem-description)
2. [Process description](#process-description)
3. [Data exploration](#data-exploration)
4. [Baseline](#baseline)
5. [Prototype](#prototype)
6. [Conclusion and perspectives](#conclusion-and-perspectives)

# Problem description

<img src="https://raw.githubusercontent.com/jamesbarthelemy/images/main/p7_desc.png" width="1200">

[Back to table of contents](#table-of-contents)

# Process description

<img src="https://raw.githubusercontent.com/jamesbarthelemy/images/main/p7_proc.png" width="1200">

[Back to table of contents](#table-of-contents)

# Data exploration

## Dataset description

<img src="https://raw.githubusercontent.com/jamesbarthelemy/images/main/p7_dataset.png" width="600">

1. The dataset used comes from the site https://www.abcbourse.com/
2. It contains the daily evolution of the EDF stock market price
3. From January 2006 to February 2022
4. 4136 lines / 6 variables

[Back to table of contents](#table-of-contents)

## Data preparation

<img src="https://raw.githubusercontent.com/jamesbarthelemy/images/main/p7_preparation.png" width="600">

[Back to table of contents](#table-of-contents)

## Feature engineering

<img src="https://raw.githubusercontent.com/jamesbarthelemy/images/main/p7_features.png" width="600">

[Back to table of contents](#table-of-contents)

### Target

<img src="https://raw.githubusercontent.com/jamesbarthelemy/images/main/p7_target.png" width="600">

1. The target variable takes the values 0 or 1
2. It is worth 0 if the closing price of the security decreases the next day
3. 1 if it increases
4. The 2 target classes are almost perfectly balanced

[Back to table of contents](#table-of-contents)

### Seasonality

<img src="https://raw.githubusercontent.com/jamesbarthelemy/images/main/p7_season.png" width="600">

There is low seasonality in the data and the trend does not contain a recurring pattern

[Back to table of contents](#table-of-contents)

# Baseline

## Test process description

<img src="https://raw.githubusercontent.com/jamesbarthelemy/images/main/p7_baseline_desc.png" width="1200">

[Back to table of contents](#table-of-contents)

## Result

<img src="https://raw.githubusercontent.com/jamesbarthelemy/images/main/p7_baseline_res.png" width="600">

[Back to table of contents](#table-of-contents)

# Prototype

## arXiv article

<img src="https://raw.githubusercontent.com/jamesbarthelemy/images/main/p7_arxiv.png" width="1200">

[Back to table of contents](#table-of-contents)

## Model description

<img src="https://raw.githubusercontent.com/jamesbarthelemy/images/main/p7_model.png" width="1200">

[Back to table of contents](#table-of-contents)

## Results

<img src="https://raw.githubusercontent.com/jamesbarthelemy/images/main/p7_results.png" width="600">

[Back to table of contents](#table-of-contents)

## Optimization

<img src="https://raw.githubusercontent.com/jamesbarthelemy/images/main/p7_tuning.png" width="600">

[Back to table of contents](#table-of-contents)

## Final result

<img src="https://raw.githubusercontent.com/jamesbarthelemy/images/main/p7_final1.png" width="600">
<img src="https://raw.githubusercontent.com/jamesbarthelemy/images/main/p7_final2.png" width="600">

[Back to table of contents](#table-of-contents)

# Conclusion and perspectives

The final performance of the prototype is slightly better than the initial performance of the baseline but still remains modest and would not allow use in production.

This can certainly be explained by:
1. The relatively small amount of data available for training the model compared to the complexity of the problem.
2. Data focused only on one stock in a much larger market and likely with hidden correlations and dependencies.
3. Data with low seasonality and no recurring pattern in the trend.

The prospects for trying to improve this situation would be:
1. Expand sources of financial data to include other securities, indices related to the industrial sector, local (relating to the local market) and international indices, currencies.
2. Also take into account technical information and/or comments on this security, its market.
3. Take local and international news into account.

[Back to table of contents](#table-of-contents)
