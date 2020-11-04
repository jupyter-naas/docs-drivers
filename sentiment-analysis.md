---
description: Get sentiment for each value in a column of the dataframe
---

# 🥰Sentiment

## Get

This will return the dataframe with a column with values `Positive, Negative or Neutral` and the score depending on the sentiment of the corresponding column value.

Exemple of data in dataset:

| Dialogue | Sentiment | Score |
| :--- | :--- | :--- |
| The lunch was delicious | Positive | 0.5719 |
| I had a bad day | Negative | -0.5423 |

```python
naas_drivers.sentiment.get(
        dataset=dataset,
        column_name="Dialogue",
        details= False
)
```

## Categorize

Define if sentiment is `positif`, `neutral` or `negatif`

```python
sentiment = 0.05
result = naas_drivers.sentiment.categorize(sentiment)
```

