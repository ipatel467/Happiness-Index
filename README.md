# Happiness-Index
###### by Ibrahim Patel




![Alt Text](https://media.giphy.com/media/5GoVLqeAOo6PK/giphy.gif)
## Executive Summary
On a scale of 1 to 10, can you rate how happy you are? The number you say is your happiness score. We decided to investigate how the happiness score varies around the world, and what factors play a role in determining a person's happiness. There are certain features that can help predict a person’s happiness such as GDP, Health, Family, Freedom, etc. We created an impressive model that captures over 90% of the data needed to predict the happiness score.

## Contents
1. [Introduction](#introduction)
    - [Problem Statement](#problem_statement)
    - [Dataset](#dataset)
2. [Analysis](#analysis)
    - [Data Cleaning](#data_cleaning)
    - [Exploratory Analysis](#exploratory_analysis)
    - [Modeling](#modeling)
    - [Results](#results)

## Introduction <a name="introduction"></a>


<p></p>

<p></p>

### Problem Statement <a name="problem_statement"></a>
Some say "Happiness is the best form of wealth", so it is only right for us to delve a little deeper into finding what makes people truly happy. There are certain features taken into account such as Country, Health, Family, Freedom, etc. There are over 7 billion people in the world, so we wanted to see how our responses would vary. We will use a Supervised Learning Regression approach for this specific model because we are trying to predict the Happiness Score which is a continuous value. 


### Dataset <a name="dataset"></a>
Here is a link to the dataset :
https://www.kaggle.com/unsdsn/world-happiness

This dataset is from Kaggle.com. 

## Analysis <a name="analysis"></a>

### Data Cleaning <a name="data_cleaning"></a>

Thankfully this dataset did not contain any null values. Overall this dataset was clean from the start which is a good thing for us. 

### Exploratory Analysis <a name="exploratory_analysis"></a>

Here is a distribution of the "Happiness Score". The "Happiness Score" is a score a person declares themselves when the question is asked, "On a scale of 1 to 10, can you rate how happy you are?". From this distribution, we can see that it looks somewhat normal.

 
![Screen Shot 2020-11-04 at 9 49 31 AM](https://user-images.githubusercontent.com/52756457/98133428-35608880-1e83-11eb-9621-65b4d1284eee.png)

Here is a distribution of the "GDP Per Capita" in the dataset. We can see that it is skewed to the right. This is due to the reason that there are more countries with higher GDPs than lower. They say "Money can't buy happiness", but it definitely has an effect on happiness.

![Screen Shot 2020-11-04 at 9 49 46 AM](https://user-images.githubusercontent.com/52756457/98133494-4a3d1c00-1e83-11eb-9643-f855db6953e2.png)

Below is the distribution of the "Freedom" feature. Once again, we can see that this distribution is skewed to the right. This is showing that there are more countries that feel that they have a high sense of freedom. This is a good thing because people everywhere should have the freedom to make life choices. 


![Screen Shot 2020-11-04 at 9 49 51 AM](https://user-images.githubusercontent.com/52756457/98133574-59bc6500-1e83-11eb-8cbf-fdfcfc0480ab.png)




### Modeling <a name="modeling"></a>
I took an Supervised Learning Regression approach when doing this problem. I used many different regressor model, and picked the ones that gave me the best results. I ran certain algorithms such as Adaboost, XGBoost, Gradient Boost, Random Forest, and Linear Regression. 
![Alt Text](https://media.giphy.com/media/6wa5vuYvetU1Jibm13/giphy.gif)



### Results <a name="results"></a>

![Screen Shot 2020-11-04 at 9 47 58 AM](https://user-images.githubusercontent.com/52756457/98133614-68a31780-1e83-11eb-8f81-54bb9329bb8f.png)
Here is the feature importance for the XG Boost model after it has been tuned. We can see that there are a few slight differences that are hard to spot right away. We can see that the "Family" feature is just very slightly less "important" than it was in our vanilla model. Also in our vanilla model, it showed that " Freedom" was the 3rd highest ranked score on feature importance. However, the XG Boost model after tuning shows that "Dystopia Residual" is the 3rd highest while "Freedom" is ranked 4th highest. 


The final model I will be going into today is the Gradient Boosting model. Once again a picked a few different hyperparameters I could mess with to see how I can improve my results. Once again my results improved ever so slightly. I received an R-Squared of 0.86 which means my model is obtaining 86% of the information needed to predict the "Happiness Score". However, the thing I find most intriguing about this model is its feature importance.



![Screen Shot 2020-11-04 at 9 47 26 AM](https://user-images.githubusercontent.com/52756457/98133674-7eb0d800-1e83-11eb-8469-6688e0b14a5e.png)


We can see that the "Dystopia Residual" takes second place in feature importance. This was interesting to see because in the other models we saw that "Dystopia Residual" was usually ranked 3rd-4th. For this AdaBoost model, it is the second more important feature. This was quite interesting to see. One final finding was the importance score for "Trust". In all the models we saw that trust had a very low importance score. However, in this model we can see that the "Trust" feature is even smaller than in the other models. "Trust" in gradient boosting is almost half of "Trust" compared to the other models, and "Trust" was always the least important feature in all the models. This is a small detail, but I found it interesting. 



To view the full extent of my work you are more than welcome to browse through the notebook. To get a better understanding of my findings to feel free to read my blog at 
https://www.ibbysblog.com/. 

I will work on this project in the future, and try my best to make my model better by doing more feature engineering.


