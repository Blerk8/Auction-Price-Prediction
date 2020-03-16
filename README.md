# Auction-Price-Prediction
Predicting the auctioned sales-price of heavy machinery (bulldozers) based on its attributes

## 1. Problem definition
The following is taken from the Kaggle Bluebook for Bulldozers competition: https://www.kaggle.com/c/bluebook-for-bulldozers/overview/description

The goal of the contest is to **predict the sale price** of a particular piece of heavy equiment at auction based on it's usage, equipment type, and configuaration. The data is sourced from auction result postings and includes information on usage and equipment configurations.

Fast Iron is creating a "blue book for bull dozers," for customers to value what their heavy equipment fleet is worth at auction.

"How well can we predict the future sale price of a bulldozer through using its charateristics and historical data."

## 2. Data
The following is taken from the Kaggle Bluebook for Bulldozers competition: https://www.kaggle.com/c/bluebook-for-bulldozers/data

**The data for this competition is split into three parts:**

Train.csv is the training set, which contains data through the end of 2011.
Valid.csv is the validation set, which contains data from January 1, 2012 - April 30, 2012 You make predictions on this set throughout the majority of the competition. Your score on this set is used to create the public leaderboard.
Test.csv is the test set, which won't be released until the last week of the competition. It contains data from May 1, 2012 - November 2012. Your score on the test set determines your final rank for the competition.

**The key fields are in train.csv are:**
SalesID: the uniue identifier of the sale
MachineID: the unique identifier of a machine. A machine can be sold multiple times
saleprice: what the machine sold for at auction (only provided in train.csv)
saledate: the date of the sale
There are several fields towards the end of the file on the different options a machine can have. The descriptions all start with "machine configuration" in the data dictionary. Some product types do not have a particular option, so all the records for that option variable will be null for that product type.

Also, some sources do not provide good option and/or hours data. The machine_appendix.csv file contains the correct year manufactured for a given machine along with the make, model, and product class details. There is one machine id for every machine in all the competition datasets (training, evaluation, etc.).

## 3. Evaluation

The following is taken from the Kaggle Bluebook for Bulldozers competition: https://www.kaggle.com/c/bluebook-for-bulldozers/overview/evaluation

The evaluation metric for this competition is the RMSLE (root mean squared log error) between the actual and predicted auction prices.

* Have a header: "SalesID,SalePrice"
* Contain two columns
  * SalesID: SalesID for the validation set in sorted order
  * SalePrice: Your predicted price of the sale
**Note:** The goal for most regression projects are to minimize the error. For example, our goal in this project is to build a machine learning model that minimises the RMSLE (root mean squared log error).

## 4. Features
Kaggle provides a data dictionary detailing the features of the dataset (filename = Data Dictionary.xlsx) via https://www.kaggle.com/c/bluebook-for-bulldozers/data

## 5. Conclusion
With fair accuracy (MSAE) we are able to predict the auction sale price of bulldozers, based on historical information.
