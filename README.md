# DSND-capstone-project

### Introduction 
This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.

From the data, different customers make decisions on whether to buy or not to buy coffee. some of the bahaviors of the customers might not be influenced by the promotional offers. However in this case, I am interested in finding out how the promotions/ offers are distributed among the different customer demographics. I will also attempt ot predict how the customers will respond to the offers they receive using models. I will evaluate the different characteristics of the customers adn how the offers are distributed amongst them.

This project is part of my Udacity Data Scientist Nanodegree program.

### Libraries used
- pandas
- numpy
- matplotlib
- seaborn
- sklearn
- json
- math
### Datasets overview

There are three  data files:

* portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
* profile.json - demographic data for each customer
* transcript.json - records for transactions, offers received, offers viewed, and offers completed

#### **portfolio.json**
* id (string) - offer id
* offer_type (string) - type of offer ie BOGO, discount, informational
* difficulty (int) - minimum required spend to complete an offer
* reward (int) - reward given for completing an offer
* duration (int) - time for offer to be open, in days
* channels (list of strings)

The portfolio dataset only contains 10 records/ rows and 6 columns. There are no missing values. The channel feature contains categorical variables that will be important for our ML model. I will therefore perform some cleaning and data encoding on it ot ensure that it is usable in my model.


**profile.json**
* age (int) - age of the customer 
* became_member_on (int) - date when customer created an app account
* gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
* id (str) - customer id
* income (float) - customer's income

**transcript.json**
* event (str) - record description (ie transaction, offer received, offer viewed, etc.)
* person (str) - customer id
* time (int) - time in hours since start of test. The data begins at time t=0
* value - (dict of strings) - either an offer id or transaction amount depending on the record


The medium article on the data analysis is [here] (https://3liud.medium.com/starbucks-capstone-challenge-ed1b35fb08be)
