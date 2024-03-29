# DE4S_Model
## A Novel Approach to Time-series Forecasting
DE4S is a novel time-series forecasting model capable of forecasting
time-variant seasonal structures. DE4S addresses common challenges in
forecasting time-variant seasonal structure by leveraging
HMM's to identify and "memorize" seasonal patterns and their 
relative likelihood.<br>

<b> Example of memorized seasonal structures:</b><br>
 ![alt text](https://github.com/kmana1995/DE4S_Model/blob/master/Images/Memorized_Structures.jpg?raw=true)<br>
 Each arrow represents the probability of transitioning between
 seasonalities<br>

## Competitive Accuracy
The model has been shown to forecast with competitive accuracy 
when compared to other widely used forecasting methods. See a comparison
of DE4S and the widely used Facebook Prophet model:<br>
![alt text](https://github.com/kmana1995/DE4S_Model/blob/master/Images/DE4S_vs_prophet.jpg?raw=true)<br><br>

## Easy, Repeatable Forecasting
Running a forecast is made simple. Required parameters include a dataframe 
containing the dependant variable and date column (df), the
dependant variable name (endog), a date header (date), the initial level 
(level), level smoothing (alpha), trend (trend), and trend smoothing (beta)
parameters. <br><br>

<b> Example:</b> <br>
Initialize:<br>
model = SeasonalSwitchingModel(df, endog, date, level, alpha, trend, beta)<br>

Fit:<br>
fitted_model = model.fit_seasonal_switching_model()<br>

Predict:<br>
fitted_model.predict(n_steps)<br>

Plot seasonal structures:<br>
fitted_model.plot_seasonal_structures()<br><br>


Package dependencies are found in the requirements.txt.

## Read the Paper
A detailed paper describing the method and mathematics can be found at https://github.com/MBAn-Applicant/DE4S_Model/blob/main/MBAn%20Forecasting%20With%20Memorized%20Seasonal%20Structures.pdf
