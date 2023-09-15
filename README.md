<h1> Stock Insights and Portfolio Refinement </h1>
#Introduction

The goal of the project is to evaulate multiple models to come up with a stocks reccomendataion system. For this we've considered top 10 stock weightes from S&P500. These stocks are then evaluated against each of the ML models with below technical indicators. The choice of technical indicators is a result of research and development across multiple research papers and trial and error methods. The models are then trained and compared on their performance on the test and train dataset. 

Most of our models are trying to solve binary classification problem defined as below: 
1. If the Adj. Close price on Friday > Adj. Close on Monday : We labeled it as "1" for action "Buy" 

2. If the Adj. Close price on Friday < Adj. Close on Monday : We labeled it as "0" for action "Sell" 

Our Ensemble model is used to finally used to compute the best performing model for below classification techniques:- 
1. Random Forests 
2. Logistic Regression
3. Boosting
4. SVC 

Since stock prices are highly time-dependent, we also considered LSTM model as an option to solve our problem, as it could predict future values based on previous sequential data and allow more parameters to be learned and contained in the model than other neural networks by adding long-term memory. However, LSTM returns numerical values (predicted future stock prices) instead of suggestion labels (buy or sell), which makes it hard to be included in the ensembled model. LSTM also has other issues, such as heavy computing power requirement (a fresh LSTM model needs to be trained and tested each time when a new individual stock is picked) and training data reliability (longer duration of stock price history may differ the result). 

**Assumptions**

Below stock data has been considered 

Start Date for dataset - 1st April 2021

End Date for dataset - 1st December 2022
<h2> Architeture </h2> 

![alt text](https://github.com/vritansh/portfoliooptimization/blob/main/ArchitectureStockPortfolioManagement.drawio.png?raw=true)
