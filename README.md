# IRCTC Stock Price Prediction

This project focuses on predicting the price movement of **IRCTC (Indian Railway Catering and Tourism Corporation)** stock using technical analysis and machine learning. The project leverages the `pandas_ta` library for calculating technical indicators and `scikit-learn` for preprocessing and modeling.

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Tech Stack](#tech-stack)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Dataset](#dataset)
6. [Methodology](#methodology)
7. [Results](#results)
8. [Contributing](#contributing)
9. [License](#license)

---

## Project Overview
The goal of this project is to predict whether the IRCTC stock price will rise or fall based on historical price data and technical indicators. The following steps are performed:
1. **Data Preprocessing**: Calculate technical indicators such as RSI, Moving Averages, Parabolic SAR, and ADX using `pandas_ta`.
2. **Feature Engineering**: Create features like price differences, moving averages, and volatility measures.
3. **Model Training**: Split the data into training and testing sets, standardize features, and train a machine learning model.
4. **Prediction**: Predict the price movement (rise or fall) for the next day.

---

## Tech Stack
- **Programming Language**: Python
- **Libraries**:
  - `pandas`: Data manipulation and analysis.
  - `numpy`: Numerical computations.
  - `pandas_ta`: Technical analysis indicators.
  - `scikit-learn`: Data preprocessing and machine learning.
  - `matplotlib`/`seaborn`: Data visualization.
- **Machine Learning**: Binary classification (e.g., Logistic Regression, Random Forest).
- **Version Control**: Git/GitHub

---

## Installation
To run this project, you need to install the required libraries. Follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/irctc-price-prediction.git
   cd irctc-price-prediction
   ```

2. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

   Alternatively, install the libraries manually:
   ```bash
   pip install pandas numpy pandas_ta scikit-learn matplotlib seaborn
   ```

---

## Usage
1. **Prepare the Dataset**:
   - Ensure you have a CSV file containing historical stock data for IRCTC (e.g., `IRCTC.NS.csv`).
   - The CSV file should have the following columns: `Date`, `Open`, `High`, `Low`, `Close`.

2. **Run the Script**:
   - Execute the `data_preprocessing.py` script to preprocess the data and train the model:
     ```bash
     python data_preprocessing.py
     ```

3. **View Results**:
   - The script will output the training and testing accuracy of the model.
   - Visualizations of key indicators (e.g., RSI, Moving Averages) can be generated using `matplotlib` or `seaborn`.

---

## Dataset
The dataset used in this project is historical stock price data for IRCTC, obtained from sources like Yahoo Finance or NSE. The dataset should include the following columns:
- `Date`: The date of the stock price.
- `Open`: The opening price of the stock.
- `High`: The highest price of the stock for the day.
- `Low`: The lowest price of the stock for the day.
- `Close`: The closing price of the stock.

Example dataset:
```
Date,Open,High,Low,Close
2023-01-01,100.0,105.0,95.0,102.0
2023-01-02,102.0,108.0,98.0,106.0
...
```

---

## Methodology
1. **Data Preprocessing**:
   - Calculate technical indicators using `pandas_ta`:
     - RSI (Relative Strength Index)
     - Moving Averages (MA, EMA)
     - Parabolic SAR (Stop and Reverse)
     - ADX (Average Directional Index)
   - Create additional features like price differences and volatility measures.

2. **Feature Engineering**:
   - Generate target variable (`Price_Rise`): 1 if the next day's closing price is higher, else 0.
   - Standardize features using `StandardScaler`.

3. **Model Training**:
   - Split the data into training and testing sets.
   - Train a binary classification model (e.g., Logistic Regression, Random Forest).

4. **Evaluation**:
   - Evaluate the model using accuracy, precision, recall, and F1-score.

---

## Results
- **Model Performance**: The model achieves an accuracy of X% on the test set.
- **Key Indicators**: Visualizations of RSI, Moving Averages, and other indicators are provided in the `visualizations/` folder.
- **Predictions**: The model predicts whether the stock price will rise or fall for the next day.

---

## Contributing
Contributions are welcome! If you'd like to contribute, please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes and push to the branch.
4. Submit a pull request.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments
- [pandas_ta](https://github.com/twopirllc/pandas-ta) for technical analysis indicators.
- [scikit-learn](https://scikit-learn.org/) for machine learning tools.
- [Yahoo Finance](https://finance.yahoo.com/) for providing historical stock data.

---

For any questions or feedback, please open an issue or contact the me.

Happy coding! 🚀
