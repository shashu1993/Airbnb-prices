# Airbnb-prices
Predicting prices for Airbnb ranked 2nd in class and 22nd overall in batch.

Using the linear regression model helped me reach a score of RMSE -65. 

I tried squaring the values for co-relations but the model had overfit my numerous variables. 
Thus, at this point I decided to move on to random forest.

Random forest was useful in getting my score down to around RMSE-60 but there was a problem that I couldn’t select variables which had more than 53 factors, hence I think I had to drop an important predictor neighbourhood_cleansed.

I initially put the number of trees to 100 and then increased to 150 and 200 but there was not much significant difference on the scores. It has to be noted that I had not engineered the zipcode and transit variables yet.
Random forest took very long(about 1.5 hours) to run the model due to which I was not too excited to continue with it

I moved on to Gradient boosting model, which was notorious for overfitting but due to its shorter running speed I preferred this over the randomForest.
Fine tuning this model proved quite a challenge. I started with 1000 trees and 1 interactions and shrinkage value of 0.01.
I actually got an RMSE of 90 after this which was depressing!
But after reading about gbm(), I increased the interactions to 8 and the shrinkage to 0.001 eventually. Because of the low shrinkage value, I had to drastically increase my trees to 30000! I did not reach to 30000 trees in one go but I reached there eventually since I could see improvements in my RMSE.

The final result was an RMSE of 55 and this help me get 2nd rank in class and 22nd overall in the Kaggle competition.
