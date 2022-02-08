# Predicting on time shipping with Machine Learning

## Introduction

This research project focused on how to apply Machine Learning to make predictions regarding shipping on time, from an international e-commerce company to their customers. Using logistic regression and train/testing method with building three models to predict the shipping, we want to discover key insights from which factors significantly affect ‘Reached on time’ and predict whether a product will be delivered on time or not.

With the globalization of trade, transit time reliability has become a critical point in the shipping industry as irregularities will lead to more delays further down the supply chain. The company that sells electronic products provides freight forwarding services to its clients, offering them a complete set of supply chain solutions for shipping their goods across the world.

Using Machine Learning computing, we developed a model capable to predict on time shipping. Our model delivers predictions with a 68% accuracy as early as the transport is booked. The model relies on historical data, for example, cost of the product, product’s weight, prior purchase, discount… We researched and tested several Machine Learning algorithms in order to select the one that maximizes the prediction accuracy score. This algorithm introduces a prediction component to the output by giving an estimated on time delivery to the customer for a shipment.

## Methodology & Results

To answer the research question about which factor(s) significantly affect reach on time, we used Logistic Regression model. Logistic Regression model describes and estimates the relationship between a dependent variable Y, which takes only two possible values, resulting from the occurrence or not of an event, and independent variables affecting that phenomenon. Its popularity is supported by the lack of necessity to meet many requirements for linear regression and general linear models, which include the linearity of the relationship between a dependent and an independent variable, as well as normality and homoscedasticity of the distribution of independent variables or the necessity to use the variables given using the metric system of measures.

To answer the research question about how to use Machine Learning to predict whether a shipment will be delivered on time or not, we apply the training/testing method with three models Logistic Regression, Decision Tree, and SVM. After running the models, we will choose and pick the best model base on the accuracy score.
We selected statistically significant variables to tie our model. To test and validate the performance of the different algorithms, we split the data in a training set and a test or validation set. All algorithms were trained and tested on the same training and test set so that we could compare their performance. Appendix G shows how we used the test and train method using Google Colab.

Then we apply three model’s Logistic regression, Decision tree, SVM.

We used Python programming language to write the code for our models. To create, train and use the final models for prediction, there are three relevant scripts in the final program. The first script is used to clean the data, remove missing values and transform all columns to the right format, our dataset has no missing value, so we don’t do this part. The second script automatically reads in all the relevant data, trains (on new data or adding data to an existing model), and saves the final model. The third script is used for prediction in a production environment. 

To predict on time shipping, we apply on three model’s Logistic regression, Decision tree, SVM.

## Model selection

|          Model	    |Accuracy Score	|Type I error|
|---------------------|---------------|------------|
|Logistic Regression	|64%	          |454         |
|Decision Tree	      |68%	          |65          |
|SVM	                |64%	          |333         |

Compare three models, we see that Decision Tree model has the highest accuracy score and lowest type I error. We will choose this model to predict the on time shipping on our dataset.

## Conclusion and future works

### Relationship between feature variables and target variables

+  Cost of the product, Prior purchases, Discount offered, Weight in gram and Product important function have a significant influence on the model, especially Cost of the product and Prior purchases. It is good to see our machine learning model match what we have been assuming.

+ Cost of the product has a negative influence on the prediction, higher Cost of the product is correlated with a not on time shipment, higher on Cost of the product, less on not on time shipment.  

### Predict on time shipment

After comparing the results yielded by three different algorithms (Decision Tree, Logistic Regression, and SVM), we decided to build the final prediction model with a Decision Tree algorithm. We selected the set of Decision Tree model as they result in the highest accuracy score (68%) and the least type I error (65), depending on the model segments. 

Not only does the Decision Tree model performs better on predicting the target variable, it is also easier to train and implement in a production system. The time required to train the Decision Tree model is less than for the SVM.

### Limitations of our approach 

Machine Learning is a method that is rather data-intensive in two ways: It requires a lot of data in order to kick-start the analysis and modeling and it requires that this data be of at least moderate and at best great quality. For great quality to be achieved, this means there should be no missing or wrong data points in the dataset, as well as consistent and useable formatting of the data. If not, the length of the data cleaning part of the project might be considerably extended, which could pose a timing problem, especially if the project is bound in time.

Furthermore, developing such a model demands analytics and coding skills. These two skills, even if required, are not enough: having subject-matter experts providing input on the industry practices and interpreting results and data is crucial to the success of such an endeavor.

Looking further down the road, since the end goal of a project like ours is to supply a functioning tool, this means the company will have to work on the models to make them a part of their computing environment. For example, the models we are delivering draw their data from several Excel files but in the future, we can imagine a direct link to a database instead.

### Potential future works

In this study, we limited our scope to electronic products, but the same models developed for this purpose could be used for any products, given that the models are trained and supplied with the appropriate data. Consequently, the relevant factors we have identified as impactful for predicting on time shipping, such as cost of the product or prior purchases, in these models are relevant for any other products.

Furthermore, another insight of our study is that our approach could be applied to any shipping industry. We could envision a similar project being conducted for the other industry for example. As long as the necessary data is available and the impactful factors can be identified, the method can be adapted for any field of industry.

In the future, it would be worth investigating the possibility of including weather patterns in the model to improve its accuracy, if access to reliable data can be guaranteed. Another way to improve the model would be to know the area of customers. This is the area of the customers where products will be delivered to. We are confident that this would increase the accuracy of the model even more.



