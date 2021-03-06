# Preliminary Analysis between FFPI and US Fx

## Initial comments regarding the project

* From the preliminary analysis and background research, the
  correlation between the FFPI and the USFX maybe by construction. The
  construction of the FFPI is based on the price of multiple
  commodities on the international market denoted in USD, as a result,
  an appreciation of the USD will result in the lowering the relative
  cost of commodity holding everything constant. This phenomenon is
  supported by the preliminary analysis that there is a negative
  correlation between the price and exchange rate and the exchange
  rate lead the FFPI by one period (month).

* Just like the commodity price is affected by random weather shocks,
  the exchange rate market also subject to the violent and volatile
  exchange rate market. You are better off predicting the FFPI
  directly rather than accumulating the error of both model.

* Based on my basic understanding, the price is driven by a large
  amount of factor which forms the expectation of the supply and
  demand. The formulation of the expectation is complex and models
  such as neural network or ensemble model are better aligned with the
  aim of the forecast. LASSO or regularised model can be used to
  identify factors which are key drivers.

* Knowing the FFPI is constructed from multiple commodity prices, it
  would also make more sense to construct the prediction for each
  composite commodity group then construct the prediction based on the
  FFPI formula.

* The current prediction for cereals seems satisfactory but will need
  a benchmark.

* Also from the analysis, it seems the nature of the time series has
  changed dramatically over time. A model which captures the varying
  coefficient or a learning model should be required.

* Since the cereals index is constructed based on the IGC wheat index,
  it makes more sense to predict the IGC wheat index then construct
  the prediction of the cereal price index.

## Questions to be answered

* How is the FFPI constructed, what are the data sources?

* What are the factors that drive the commodity price, this depends on
  how the index is constructed.

* Price of competing commodity such as US bond, and oil price should
  also be considered.


* Consider the option of forecasting the commodity price from the
  FBS/CBS. This can be the starting point for predicting the trend and
  a starting point to understand the mechanism.



## Potential solution

* Prediction based on FBS/CBS

1. Construct a monthly FBS by maximising the correlation between the
  FBS and the FFPI.

2. Time series forecast the FBS

3. Predict the FFPI based on the FBS.

* Prediction based on neural network

1. Use LASSO to select grid points and time which arae relevant for
predictin the production.

2. Constructe the factor datasets which are relevant for predicting
the expectation of the price and feed it into the neural network.

------------------------------------------------------------------------

Second meeting with Adam:

New insights:

1. It appears that the exchange rates are not good predictors nor they
appear to drive the price of wheat. The data shows that the rolling
correlation between the variables can range from -1 to +1. Further
from the running correlation, it would suggests that there does not
have a meaningful model in the linear sense, and if any link is to be
established, it would have to be non-linear.

2. The Cross-correlation function also suggests that exchanges rate is
not the lead variable, rather it is the lagged variable if there is
any relationship.

3. It would appear that the exchange rate only correlates highly with
the wheat price over certain period. In particularly during the food
price crisis over the period from 2007 to 2008.

4. There seems to be high correlation and predictive power when the
crude oil price is included in the explanatory set.


Questions:

* What should we do next? I think we need to continue to explore other
  possible explanatory variables such as production. Can explanation
  can be done without a good model. But at least we know that exchange
  rate does not have a major role in driving the price of wheat.