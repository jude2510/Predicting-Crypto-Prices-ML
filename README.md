# Cryptocurrency Forecasting and Correlation Analysis

This repository contains two exploratory projects that apply machine learning and statistical analysis techniques to the cryptocurrency market. The first project uses a Long Short-Term Memory (LSTM) neural network to predict Bitcoin (BTC) prices, while the second project explores the correlation between Bitcoin and Ethereum (ETH) using Principal Component Analysis (PCA).

📄 [Project Report (PDF)](./ProjectReport.pdf)

---

## 🧠 Project 1: Predicting Bitcoin (BTC) Prices with LSTM

### Overview
With Bitcoin’s volatility and growing market influence, accurate price prediction is essential for traders and investors. This project leverages LSTM neural networks—a specialized form of recurrent neural networks (RNNs)—to forecast daily Bitcoin closing prices based on historical data.

### Data
- Source: [Kaggle Dataset – Crypto Prices](https://www.kaggle.com/datasets/svaningelgem/crypto-currencies-daily-prices)
- Features used: Daily **closing prices** (focus), along with OHLC data

### Preprocessing
- Cleaned missing data
- Applied `MinMaxScaler` to normalize closing prices between 0 and 1
- Used 60-day input sequences to predict the next day’s closing price

### Model Architecture
- Framework: Keras (TensorFlow backend)
- Two stacked LSTM layers
- Dropout layers to prevent overfitting
- Dense output layer with one neuron

### Results
- Predicted prices closely aligned with actual market prices
- Visualization showed that the LSTM model captured underlying temporal dynamics well

### Future Scope
- Extendable to other cryptocurrencies
- Can incorporate additional financial indicators
- Could benefit from tuning hyperparameters or using transformer models

---

## 📊 Project 2: Correlation Analysis Between Bitcoin and Ethereum

### Overview
This analysis investigates the relationship between BTC and ETH price movements using Principal Component Analysis (PCA), a dimensionality reduction technique that reveals patterns in multivariate data.

### Data
- Daily closing prices from Ethereum’s launch (August 2015) to present
- Standardized using `StandardScaler` to zero-mean and unit-variance

### Method
- PCA applied to standardized BTC and ETH price series
- Scree plot and biplots used for analysis

### Results
- First principal component explained ~95% of total variance
- Biplot showed BTC and ETH separated by ~45°, suggesting **moderate positive correlation**
- Confirmed shared trends but distinct dynamics

### Implications
- Highlights value in diversification between BTC and ETH
- Confirms co-movement patterns while retaining currency-specific drivers

---

## 📈 Tools & Libraries

- Python 3.x
- Pandas, NumPy
- scikit-learn (PCA, scalers)
- Keras & TensorFlow (LSTM)
- Matplotlib, Seaborn (visualization)

---

## 🔗 References

- [Kaggle: Crypto Prices Dataset](https://www.kaggle.com/datasets/svaningelgem/crypto-currencies-daily-prices)
- [LSTM Neural Networks – Wikipedia](https://en.wikipedia.org/wiki/Long_short-term_memory)
- [Crypto Forecasting with LSTMs – Towards Data Science](https://towardsdatascience.com/cryptocurrency-price-prediction-using-lstms-tensorflow-for-hackers-part-iii-264fcdbccd3f)
- [Investopedia: Bitcoin vs Ethereum](https://www.investopedia.com/articles/investing/031416/bitcoin-vs-ethereum-driven-different-purposes.asp)

---

## 📄 License

MIT License


