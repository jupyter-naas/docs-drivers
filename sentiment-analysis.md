---
description: Get sentiment for each value in a column of the dataframe
---

# 🥰Sentiment Analysis

```python
dataset = pd.DataFrame(
        data={
                "id": [1, 2],
                "Dialogue": [
                        "The lunch was delicious",
                        "I had a bad day"
                ]
        }
)
naas_drivers.sentiment_analysis().calculate(
        dataset=dataset,
        column_name="Dialogue",
        details= False
)
```

This will return the dataframe with a column with values `Positive, Negative or Neutral` and the score depending on the sentiment of the corresponding column value.

| Dialogue | Sentiment | Score |
| :--- | :--- | :--- |
| The lunch was delicious | Positive | 0.5719 |
| I had a bad day | Negative | -0.5423 |

