---
description: Predict the time series data
---

# 🔮Prediction

Give a data frame with theses columns

| Date | Close |
| :--- | :--- |
| 2014-04-14 | 133.95 |

Base data can come from Yahoo driver

{% page-ref page="product-drivers/yahoo.md" %}

## All

_**The model will predict SVR, LINEAR, ARIMA for 20 days on Close value**_

```python
dataset = naas_drivers.yahoo.stock("TSLA")
pr = naas_drivers.prediction.get(dataset=dataset)
```

## Prediction size

* `data_points`:  _**The number of days in future that are to be predict.**_

```python
dataset = naas_drivers.yahoo.stock("TSLA")
pr = naas_drivers.prediction.get(dataset=dataset, data_points=50)
```

## Model

> All the parameters of the above formula are explained below.

*  `prediction_type`:  _**The model to predict, it can be SVR, LINEAR, ARIMA, or ALL**_

```text
dataset = naas_drivers.yahoo.stock("TSLA")
pr = naas_drivers.prediction.get(dataset=dataset, prediction_type="ARIMA")
```

## Options

*  `label`:  
   _**The actual value that is to be predict.**_ 

  ```text
    Type: String
    Expected Value: The exact name of the column that is to be predicted, from the dataset.
  ```

*  `date_column`:  
   _**The date range from the dataset. Will be used as the output index.**_  


  ```text
    Type: String
    Expected Value: The exact name of the date column from the dataset.
  ```

```text
dataset = naas_drivers.yahoo.stock("TSLA")
pr = naas_drivers.prediction.get(dataset=dataset, prediction_type="ARIMA", label="Open", date_column="Date")
```

## Plot

> Once you have predicted using the above predict formula, you can plot the predictions

```python
  naas_drivers.plotly.stock(pr)
```

Check more options on the link below

{% page-ref page="product-drivers/chart.md" %}

