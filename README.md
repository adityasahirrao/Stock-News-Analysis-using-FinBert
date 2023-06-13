# Stock-News-Analysis-using-FinBert model 
Stock News Analysis using FinBert model to predict next day stock direction

The provided code is an example of a stock news analysis using the FinBert model to predict the next day's stock direction based on sentiment analysis of news headlines. The code fetches news articles related to a specific stock symbol (in this case, "AAPL" for Apple Inc.) from the Alpha Vantage API. It then cleans and preprocesses the article data by combining the title and summary, removing unnecessary brackets and special characters.

The code then utilizes the FinBert model, which is a pre-trained model specifically designed for financial sentiment analysis. The FinBert model is loaded using the transformers library, and the cleaned article data is tokenized and passed through the model to generate sentiment predictions. The sentiment scores (positive, negative, and neutral) for each article are stored in a DataFrame.

The sentiment scores are visualized using a bar chart, where each headline's sentiment is represented by the height of the corresponding bar. The sentiment scale ranges from positive (green) to negative (red) with neutral sentiment (blue) in between.

The code also determines the overall sentiment for all the headlines by selecting the sentiment category (positive, negative, or neutral) with the highest score for each article. The sentiment counts are calculated and displayed.

Furthermore, the cumulative sentiment scores are calculated by subtracting the negative sentiment score from the positive sentiment score for each headline. The cumulative sentiment trends are visualized using a line chart, showing the overall sentiment pattern across the headlines.

Finally, the code predicts the stock direction for the next day based on the cumulative sentiment score. If the overall sentiment score is positive, the predicted direction is "Up"; if negative, it's "Down"; and if the sentiment score is neutral, the predicted direction is "Neutral."

