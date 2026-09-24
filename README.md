# OPIM 5512 Lab 2 – Explaining a Model with SHAP

## Overview
### Welcome to our repository!
In this lab, we used SHAP (SHapley Additive exPlanations) to better understand a machine learning model that predicts electricity demand in MW. Instead of only looking at how accurate the model was, we focused on explaining what features were influencing its predictions. We looked at the model from both a global perspective, which explains what features matter overall, and a local perspective, which explains one specific prediction.

## What We Did

We used the model's built-in feature importance and SHAP values to compare how different features affected predicted electricity demand. The features included hour of day, temperature, dew point, humidity, weekend status, and wind speed.

For the global analysis, we created SHAP plots to see which features had the largest overall impact on the model and whether different feature values pushed predictions higher or lower. We also used a predicted-vs-actual plot to compare the model's predictions with the actual electricity demand.

For the local analysis, we used a SHAP waterfall plot to explain the hour where the model predicted the highest electricity demand. This allowed us to see exactly which features pushed that individual prediction up or down.

## Results

The results showed that *hour of day was the most important feature* in the model overall. Dew point and temperature were also important, while humidity, weekend status, and wind speed had smaller effects. The global SHAP results generally supported the model's built-in feature importance, with hour of day clearly having the strongest influence.

The SHAP beeswarm plot also showed that the effect of a feature depends on its value. For example, different hours of the day could either increase or decrease predicted electricity demand rather than having one constant effect.

For the local prediction, the model predicted about *19,390 MW. The largest factor pushing this prediction higher was **hour of day (17), which increased the prediction by about **2,862 MW. A temperature of **85°F* also increased it by about *1,133 MW, while humidity contributed about **278 MW*. Dew point and wind speed slightly lowered the prediction.

Overall, the global and local SHAP results told a similar story: *time of day was the strongest driver of the model's electricity demand predictions, while weather conditions also played an important role.*

