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

![NN3 Image 4](https://github.com/martaaliu/AFiCS-NN3-Reduced-Data/blob/main/Images/NN3%20Plot%201%20(a.3).png)

#### 4. Compare the results obtained in sections 2. and 3. and evaluate how the different methods perform across the various time series. 

The forecast accuracy results from section 2 are shown below:

<img src="https://github.com/martaaliu/AFiCS-NN3-Reduced-Data/blob/main/Images/Accuracy%20Results%20NN3%20a.PNG?raw=true" width="900">

The forecast accuracy results from section 3 are shown below:

<img src="https://github.com/martaaliu/AFiCS-NN3-Reduced-Data/blob/main/Images/Accuracy%20Results%20NN3%20a3.png" width="900">

With regards to section 2, there is not a single method that outperforms the rest for all the time series. This was expected, as every time series presents different patterns in terms of seasonality, trend and range of values which might be more suitable for one method than another. The Naïve method is the best performing method in terms of accuracy (lowest RMSE, SMAPE and MAPE values on the test set) for series NN3_106; the Holt Winters method for series NN3_101, NN3_105, NN3_107, NN3_109 and NN3_111; the Holt method with damped trend for series NN3_110; and the ARIMA method (which includes seasonal terms for some of the time series) for series NN3_102, NN3_103, NN3_104 and NN3_108. The SES method, however, did not outperform other methods for any of the series. The fact that methods which deal with seasonality generally performed better than other simpler methods is expected, since all our time series present very evident yearly seasonality.

With regards to section 3, there is also not a single method that outperforms the rest. The NNetar method performs best for NN3_101, NN3_103, NN3_104, NN3_105, NN3_106, NN3_107 and NN3_111; the MLP method performs best on NN3_108 and NN3_110 and the ELM method performs best for NN3_102 and NN3_109. The optimization of hyperparameters might result in different performance of each model.

When comparing the performance of the methods used in section 2 and 3, the methods of section 3 generally outperform the methods used in section 2 (based on RMSE, SMAPE and MAPE values on the test set). This is due to the fact that the machine learning methods fit models way better than standard linear or other statistical approaches which perform well for certain time series but that cannot be easily extended to other time series with different characteristics.
