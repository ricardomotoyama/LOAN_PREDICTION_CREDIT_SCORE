<img src="https://specials-images.forbesimg.com/imageserve/1168122573/960x0.jpg" width="700" height="300">

# Development of a credit score model

Customers' behavior from retail bank is completely different of wholesale bank. 

Whether a customer from retail bank asks some loan, the bank uses statistical models (credit score) to approve it or not. 

<img src="https://media1.tenor.com/images/54552c5f2ea273a0086079a396043128/tenor.gif?itemid=13765398" width="500" height="300">

Doing some comparison, It looks like a assembly line from a factory that produce the same part millions of times per hour with the same qualities and standards. If a part is outside of standards it will be discharged.

In the other hand, customers from Wholesale Banks are Large Corporate or Middle Market and when these customers ask some loan like working capital, analysts from Wholesale Banks evaluate some financial statements and balance sheet to approve or deny a loan.

![](https://media1.tenor.com/images/cb39c6851240eda84694c00000379f5d/tenor.gif?itemid=13765529)

In this project, a statistical model (credit score) will be developed using Logistic Regression.


### Exploratory Data Analysis (EDA)

There is a Jupyter Notebook (EDA_V4.ipynb) with exploratory data analysis. 

First analysis have done with an open source library called sweetviz. Sweetviz shows missing values, calculate skewness, kurtosis, does histograms and bar charts. It's a nice library to do some fast exploratory data analysis.

After that, more complex analysis will be presented like boxplot with logarithm natural transformation versus feature without any kind of transforation, correlation matrix, creating new features and IQR to indentify outliers.

Besides that there are some drafts about what kind of transformers (logarithm natural and dummy transformer) and scalers (robust scaler) will be used together into pipelines.



### Model with pipelines

There is a Jupyter Notebook (MODEL_PIPELINE_V0.ipynb) with all pipelines from model's development. If you never heard about pipelines lets explain a little bit.

Basically, Pipelines work like LEGO blocks. When you are doing EDA, you need to replace missing values or drop them, you need to do some transformations like logarithm natural on features, you need apply some scaler (StandardScaler, MinMaxScaler, RobustScaler) and you need some estimator. 

There are some built-in transformers on Scikit-Learn but sometimes you need a specifc transformer but don't worry about it because you can build your custom transformers using the class TransformerMixin. In this project I used some custom transformers and they are on custom_transformers.py.

The next picture helps to understand it:

![](https://iaml.it/blog/optimizing-sklearn-pipelines/images/pipeline-diagram.png)

But... Why do you use Pipelines? 

Pipelines are used into model development because:

1) It makes your code clean and easy to understand what kinds of transformers, scalers and estimators you use.

2) Pipelines avoid data leakage.

3) It makes easier the deploy of the model.


Now enjoy it!!

![gif002](https://media.giphy.com/media/xT5LMQ8rHYTDGFG07e/giphy.gif)
