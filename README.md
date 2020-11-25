# AFiCS-NN3-Reduced-Data
## Forecasting Time Series from the NN3 Reduced Dataset

The NN3 dataset is taken from here: http://www.neural-forecasting-competition.com/NN3/

The NN3 reduced time series are the following, where the test data is shown in red:

![NN3 Image 1](https://github.com/martaaliu/AFiCS-NN3-Reduced-Data/blob/main/Images/NN3%20Plot%201%20(a.1).png?raw=true)

The goal of this task is to forecast the 11 reduced time series NN3_101 to NN3_111 using different methods on R. The methods chosen are the following:
* Naïve
* Single Exponential Smoothing (SES)
* Seasonal Exponential Smoothing (Holt Winters method)
* Dampened Trend Exponential Smoothing (dampened Holt's method)
* ARIMA
* NNETAR
* MLP (Multi Layer Perceptron)
* ELM (Extreme Learning Machines)

The test data is also available on the Excel spreadsheet. Therefore, the methods will be evaluated in terms of forecast accuracy against the actual values from the test dataset. The accuracy measures employed to assess the accuracy of the different methods are RMSE, MAPE and SMAPE. 

The task is divided into 4 parts:

#### 1. Plot the data to look at some effect of the changing seasonality over time. If necessary, do an STL decomposition of the data.

![NN3 Image 2](https://github.com/martaaliu/AFiCS-NN3-Reduced-Data/blob/main/Images/NN3%20Plot%202%20(a.1).png?raw=true)

#### 2. Forecast using the following established statistical forecasting methods: Naïve, Single Exponential Smoothing, Seasonal Exponential Smoothing, Dampened Trend Exponential Smoothing and ARIMA.

![NN3 Image 3](https://github.com/martaaliu/AFiCS-NN3-Reduced-Data/blob/main/Images/NN3%20Plot%202%20(a.2).png?raw=true)

#### 3. Forecast using the following machine learning algorithms: NNETAR, MLP and ELM.

#### 4. Compare the results obtained in sections 2. and 3. and evaluate how the different methods perform across the various time series. 

Results from section 2:

<img src="https://github.com/martaaliu/AFiCS-NN3-Reduced-Data/blob/main/Images/Accuracy%20Results%20NN3%20a.PNG?raw=true" width="720">

