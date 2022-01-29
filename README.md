# ROSSMANN Store Sale Prediction
Future forecasting using ARIMA models for ROSSMANN dataset

__Files__
- train.csv - historical data including Sales
- store.csv - supplemental information about the stores

__Data fields__
Most of the fields are self-explanatory. The following are descriptions for those that aren't.

- Id - an Id that represents a (Store, Date) duple within the test set
- Store - a unique Id for each store
- Sales - the turnover for any given day (this is what you are predicting)
- Customers - the number of customers on a given day
- Open - an indicator for whether the store was open: 0 = closed, 1 = open
- StateHoliday - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None
- SchoolHoliday - indicates if the (Store, Date) was affected by the closure of public schools
- StoreType - differentiates between 4 different store models: a, b, c, d
- Assortment - describes an assortment level: a = basic, b = extra, c = extended
- CompetitionDistance - distance in meters to the nearest competitor store
- CompetitionOpenSince[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened
- Promo - indicates whether a store is running a promo on that day
- Promo2 - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating
- Promo2Since[Year/Week] - describes the year and calendar week when the store started participating in Promo2
- PromoInterval - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store

__Evaluation Matrics__
Root mean squre is selected as we wanted to avoid the larger prediction errors.

__SARIIMAX Model__

Accuracy: 
- Roost Mean Squared Error - 414.04

![image](https://user-images.githubusercontent.com/23438020/151603528-40495e16-2a9c-4d6f-a102-9bd7fd647b71.png)

__XGBOOST__

Accuracy:
- Roost Mean Squared Error - 361.06

![image](https://user-images.githubusercontent.com/23438020/151643911-83ad7839-48c3-463d-b617-82d59d9c9a69.png)


__Conclusion__
- XGBOOST Regressor is having better accuracy and it should be considered a the forecasting model.

