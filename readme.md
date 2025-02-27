# Bitcoin Price Prediction with Random Forest

This project uses machine learning to predict Bitcoin prices using historical price data. It implements a Random Forest Regressor model to forecast Bitcoin prices one hour into the future.

## Dataset

- Bitcoin price data at 1-minute intervals from 2012 to Present
- Full dataset contains over 6 million records
- For this model, we used:
  - A subset from January 2024 to September 2024
  - Resampled to 15-minute intervals
  - Features include: OHLCV data, technical indicators, and time-based features

## Project Structure

```
bitcoin_price_prediction/
├── data/                 # Contains raw and processed data
├── models/               # Saved model files
├── notebooks/            # Jupyter notebooks for exploration
├── results/              # Output figures and model performance metrics
├── src/                  # Source code
│   ├── data_prep.py      # Data preparation scripts
│   ├── features.py       # Feature engineering
│   ├── models.py         # Model training and evaluation
│   └── utils.py          # Utility functions
├── tests/                # Unit tests
├── README.md
└── requirements.txt      # Dependencies
```

## Features

- Data cleaning and preparation
- Feature engineering with technical indicators
- Time series train-test split
- Random Forest model for prediction
- Hyperparameter tuning
- Model evaluation and visualization
- Real-time prediction capability

## Key Performance Metrics

| Metric | Baseline Model | Optimized Model |
|--------|----------------|----------------|
| RMSE   | 522.19         | 523.39         |
| MAE    | 380.45         | 376.66         |
| R²     | 0.9756         | 0.9755         |

### Real-World Prediction Testing

When tested on unseen data, the model's predictions were off by approximately 0.34% or roughly $200. For example:

- Predicted price for September 17, 2024 03:00: ~$57,920
- Actual price at that time: $58,058.57 (Open: $58,100.97, High: $58,122.79, Low: $58,016.09)

This level of accuracy is quite reasonable for cryptocurrency prediction, given the inherent volatility of Bitcoin prices.

## Feature Importance

The top features for prediction are:
1. Feature 1
2. Feature 2
3. Feature 3

## Installation and Usage

1. Clone this repository
2. Install requirements: `pip install -r requirements.txt`
3. Run data preparation: `python src/data_prep.py`
4. Train the model: `python src/models.py`
5. Make predictions: `python src/predict.py`

## Future Improvements

- Implement additional models (LSTM, XGBoost)
- Add more external features (sentiment analysis, network metrics)
- Deploy as a web application for real-time predictions

## License

MIT

