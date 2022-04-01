# Classification Model, In-Vehicle Coupon

* The aim of this assignment is to build a simple classification model for the in-vehicle coupon recommendation data set from the UCI Machine Learning [repository](https://archive.ics.uci.edu/ml/datasets/in-vehicle+coupon+recommendation).
* This is a simple dataset in which the objective of the model should be to determine whether a driver would accept a coupon based on a set of features including the type of coupon.

* This data studies whether a person will accept the coupon recommended to him in different driving scenarios. 
* This data was collected via a survey on Amazon Mechanical Turk. 
* The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. For more information about the dataset, please refer to the paper:
Wang, Tong, Cynthia Rudin, Finale Doshi-Velez, Yimin Liu, Erica Klampfl, and Perry MacNeille. 'A bayesian framework for learning rule sets for interpretable classification.' The Journal of Machine Learning Research 18, no. 1 (2017): 2357-2393.

# Data Description

![alt text](https://github.com/manuzrpEd/ClassificationModel-InVehicleCoupon/blob/main/DataDescription.png?raw=true)

# Results

When we look at the data, we see that a few variables have categories with a relatively higher number of coupon acceptances. For example, 1-day expiration coupons have a relatively higher number of coupon acceptances with respect to 2-hour expiration coupons. As a second example, drivers whose destination is classified as 'Not Urgent Place' vs 'Home' or 'Work' have a relatively higher number of coupon acceptances.

<p float="left">
  <img src="https://github.com/manuzrpEd/ClassificationModel-InVehicleCoupon/blob/main/img/crosstab_expiration.png" alt="crosstab_expiration"/>
  <img src="https://github.com/manuzrpEd/ClassificationModel-InVehicleCoupon/blob/main/img/crosstab_destination.png" alt="crosstab_destination"/>
 </p>
 
 In the data, we note that there are relatively more acceptances with:

* lower income
* lower age (younger drivers)
* no children
* single marital status
* Carry out & Take away coupons + Restaurant(<$20), relative to Coffee House, Bar or Restaurant($20-$50) 
* Sunny weather as opposed to Rainy or Snowy 
* 80 temperature (higher temperature), relative to 55 or 30 temperature.

Because many of these variables may correlate with each other (for example high temperatures may coincide with sunny weather), we need to construct a model and estimate it to select the most predictive features for coupon acceptance. We can use the Logistic regression model. The probability or odds of the response variable (coupon acceptance) is modeled as function of multiple independent variables.

 	$\hat{a}$

 




