# Electric Car Price Prediction

A machine learning notebook that predicts the average price of a new car from yearly electric vehicle market indicators, using multiple linear regression in scikit-learn.

## Dataset

`Electric cars.csv` contains one row per year from 2010 to 2022 (13 rows) with these columns:

| Column | Description |
| --- | --- |
| `Year` | Calendar year |
| `BEV average price (USD)` | Average price of a battery electric vehicle |
| `Global Sales Volume` | Worldwide electric vehicle sales |
| `Mileage (Km)` | Average range in kilometres |
| `Lithium Ion Battery Price (USD)` | Battery price |
| `Average price of new car` | Target variable |

One row has a missing sales volume and is dropped before training, which leaves 12 observations.

## Method

1. Load the CSV with pandas and standardise the column names.
2. Check data types, unique values, missing values and the distribution of the target with Seaborn.
3. Drop rows with missing values.
4. Use the first five columns as features and the average new car price as the target.
5. Split into training and test sets (80 / 20, `random_state=0`).
6. Fit a `LinearRegression` model and predict on the test set.

## Results

| Metric | Value |
| --- | --- |
| R² on the training set | 0.942 |
| R² on the test set | 0.986 |

The dataset is very small, so the test set contains only three rows. Treat these scores as a demonstration of the workflow rather than evidence of a production-grade model. More years of data, or data broken down by market, would be needed for reliable forecasting.

## Tech Stack

- Python 3
- pandas, NumPy
- Matplotlib, Seaborn
- scikit-learn
- Jupyter Notebook

## Getting Started

```bash
git clone https://github.com/mosesaderemi/electric-car-price-prediction.git
cd electric-car-price-prediction
pip install pandas numpy matplotlib seaborn scikit-learn notebook
jupyter notebook "Electric-car Price Prediction Model.ipynb"
```

Run the cells in order. The notebook reads `Electric cars.csv` from the same folder.

## Author

Aderemi Moses Timileyin
GitHub: [@mosesaderemi](https://github.com/mosesaderemi)
LinkedIn: [linkedin.com/in/mosesaderemi-6a70a5405](https://www.linkedin.com/in/mosesaderemi-6a70a5405)

## License

Released under the MIT License. See the `LICENSE` file for details.
