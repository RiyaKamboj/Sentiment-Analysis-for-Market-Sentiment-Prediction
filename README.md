# Sentiment Analysis for Market Trend Prediction

## Project Overview
This project involves using sentiment analysis on news data to predict market trends, specifically focusing on the Dow Jones Industrial Average (DJIA). By analyzing historical news headlines and corresponding stock data, machine learning models are trained to forecast the movement of DJIA's adjusted closing price.

## Dataset Description
### Data Sources
- **News Data**: Top 25 news headlines per day from Reddit, ranked by user votes.
- **Stock Data**: Historical DJIA data used to establish a relationship between news sentiment and stock performance.

### Files Used
- **Combined_News_DJIA.csv**: News headlines with labels indicating market movement.
- **RedditNews.csv**: Daily top 25 news headlines.
- **DJIA_table.csv**: DJIA stock data including opening, high, low, and adjusted closing prices.
- **Test_DJIA_dates.csv**: Stock data used for prediction.
- **Test_Combined_news.csv**: News data used for model testing.
- **Test_Reddit_news.csv**: Test news headlines for prediction.

### Key Columns
**Combined_News_DJIA.csv**:
- **Date**: Date of publication.
- **Label**: '1' for non-decreasing adjusted close, '0' for a decrease.
- **Top1 - Top25**: The top 25 news headlines for that date.

**DJIA_table.csv**:
- **Date**: Date of the record.
- **Open/High/Low/Close**: Stock price details for the day.
- **Volume**: Number of registered trades.
- **Adj Close**: Adjusted closing price.

## Methodology
1. **Data Loading and Exploration**:
   - Load and inspect data files for insights and preprocessing needs.
2. **Preprocessing**:
   - Convert columns to appropriate data types, handle missing values, and standardize formats.
3. **Feature Engineering**:
   - Extract sentiment scores from news headlines and encode them for model training.
4. **Model Training**:
   - Use regression models (e.g., Ridge Regression) to train on combined features from news sentiment and stock data.
5. **Model Evaluation**:
   - Evaluate predictions using Mean Squared Error (MSE) to measure accuracy.

## Results
The model's performance is evaluated by comparing predicted DJIA adjusted closing prices with actual values. The MSE between predicted and actual adjusted close values was found to be substantial due to the high scale of stock prices.

## Conclusion
While the model's Mean Squared Error (MSE) may seem large, it is justified by the scale of the actual adjusted closing prices, which are typically around 17,000. This indicates the importance of considering relative error when evaluating stock market predictions.

## Future Work
- Explore advanced NLP techniques for better sentiment extraction.
- Incorporate additional features such as economic indicators or social media trends.
- Utilize more complex models like LSTM or ensemble methods for improved accuracy.

## How to Run the Code
1. Ensure Python and required libraries (`pandas`, `scikit-learn`, `yfinance`, etc.) are installed.
2. Load the project notebook and run the cells sequentially to train the model and make predictions.
3. Verify outputs using provided test data.

## Dependencies
- Python 3.x
- pandas
- scikit-learn
- yfinance
- Jupyter Notebook (for running the code)
