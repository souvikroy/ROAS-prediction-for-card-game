# ROAS-prediction-for-card-game

- Problem statement : Marketer spends thousands of $ to get sufficient amount of users for VIP Baloot(card game) whereas 2-5% users actually converts to customer(as in-app-pack purchaser) within 30days from the installation. so, marketer used to find the best performing channels as per history whereas the marketing channel behaviour is very dynamic. So, historical 30day return on marketing investment across channel does not really give accurate direction to marketer to improve the cost of acquisition of users. So, marketer of VIP Baloot hired me to build an AI predictive model which can give a direction to marketer on which channel do they focusto improve the 30 & 60day cohorted revenue from the investment.

- Solution : As concerned as the solution, I devided the entire solution into 4 parts : 1. Data extraction & discovery 2. Exploratory data analysis 3. Modeling of ROAS 4. Tuning of model and training; Below described in details

1. Data Extraction : Souce of data is adjust marketing tool : performance marketing click stream data like channel wise CTR, cohorted revenue, cohorted installs, cohorted north star usage metrics inside the game, cohorted currency monetisation metrics inside the game.

2. Exploratory data analysis : Aim is to find out gaps and opportunity in marketing across channels & correlation between north star metrics and marketing cost

Channel wise marketing insights
![image](https://user-images.githubusercontent.com/4746631/221345340-fa3cbe49-8ae3-4323-8bd8-a26db9369eaf.png)

Correlation
![image](https://user-images.githubusercontent.com/4746631/221345403-1c6a7cc4-ffb8-4b0f-9ab5-54926ff06a67.png)

3. Modeling of ROAS : Here, I wanted to predict cohorted revenue/ad spend for next 30days whereas ad spend is depending on business objective as well it should be rule based input from the user of the model and cohorted revenue is to predict here.
I devided the cohorted revenue prediction into two different parts 

(i) Prediction of revenue for cohorted period - since the revenue here is cohorted revenue whereas cohort period is 30days, we need predict the revenue across channel from those 30days.
(ii) Prediction of revenue for next 30days(future period) : Future 30days cohorted revenue based on input from marketer on 2X, 0.5X, 3X marketing spend compared to last month.

Model type : XG boost machine learning model, Pls go through the code and let me know any question.

4. Tuning & training : we can tune accuracy(%difference ROAS across channel between actual and predicted ROAS) by n_estimator which is nothing but the no of gradients as well difficulty of ML model, here, I found 250 as optimal n_estimator with 96% accuracy. I created a tuning criteria as input for marketer as well marketer can tune him/herself and get the predicted ROAS across channels
