# Back testing NSE stockmarket data and trend classification using Image Analytics

## Trend Classification 

**Step 1 :** 
### Identify up-trend , down-trend ,flat days 

* Method 1 - Linear regression of minute data 
Classification based on slope of linear regression line ( Brackets of slopes - both upward and downward)
![](https://github.com/tomtillo/BackTesting/blob/master/up_trend_Down_trend.jpg)

* Method 2 - Average of n-time period data 
Classification based on the shape of the resulting figure  ( Using convolutional neural networks )
![](https://github.com/tomtillo/BackTesting/blob/master/shape_detection_CNN.jpg)


**Step 2 :** 
Group the trend days together and overlap the images to form a combined image with a band of price movements. 
![](https://github.com/tomtillo/BackTesting/blob/master/graph_overlap.png)

## Volatility prediction
Few metrics for volatility 

* **Standard Deviation from linear regression line** 
* **Standard Deviation at average intervals of time** ( refer to the earlier discussion on trend classification )

## Back Testing 
* **70-30 train-test split**   ( preserving the time character of data )
* **70-30  with randomized train-test data**  ( cancels auto-correlation & depends on the derived variables & relationship to index prices and other stock prices in same industry )
* **3-hr data (0915 - 1200 )** ( Train on morning session data and test on post noon session )
### Steps for back testing 
* Define strategy
* Code
* Back Test on historical data
* Generate Reports
* Compare strategies

Comparison of strategies are done using same metrics defined across 
### Risk Metrics
* Max Drawdown  Amount
* Max Drawdown duration
* Sharpe Ratio

### Performance Metrics
* Net Profit (  for the period of testing)
* Profit factor (Pf)= Sum of Profit / Sum of Loss
* Outlier Adjusted Profit factor
* % winning trades 
* Wining / Loosing Streak  ( count )
* Avg Profit/Loss per trade 
* Profit %   = Total Profit / Total Invested

### Periodicity Metrics
* Number of times the events that satisfy the strategy occurs in the test period
* Average frequency per unit test period ( duration between two occurrences )




