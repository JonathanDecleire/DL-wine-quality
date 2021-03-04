### DL-wine-quality

The mission objective was to create a model to predict the quality of wine using a deep learning library. We had a choice between pytorch or keras and pytorch was chosen to challenge ourselves.

This is a solo project but the 'we' term will be used for explanation purposes. The project was to be completed in three days.

The dataset contained ~6500 rows, 11 feature columns ('fixed acidity', 'volatile acidity', 'citric acid', 'residual sugar', 'chlorides', 'free sulfur dioxide', 'total sulfur dioxide', 'density', 'pH', 'sulphates', 'alcohol') and one target column ('quality).

To begin our model building and predicting we first saw that the quality scale of wine goes from 1 to 10 (1 being the worst) and that the dataset contained quality scores from 3-9 only. This provided us with 7 different possible scores that could be assigned to the wine. From there we calculated that by random chance we had a 100/7 = 14.3% chance of guessing the correct score.

The goal is of course to build models that will provide us with a better score than just pure luck.

We first embarked on creating a linear regression model by using the sklearn module and were able to achieve a 30% score. This is already an improvement but does not add up to a model that has strong predictive capabilities.

As the purpose of the exercise is to use the deep learning module of pytorch in our case, we moved on to trying it out by using a linear regression model again. The accuracy score we achieved was 60%. Again this is a serious improvement. However we see that overfitting is occurring and that not many of the features at our disposal display a linear relationship with our target variable 'quality'.

We mapped out the different graphs of the linear relationships between the different features and the target variable quality and after careful observation concluded that only 5 out of the 11 features had strong enough linearity. We ran a new model by using only those 5 features and noted an improvement to 62% in accuracy. As we see that using a linear model to try and predict the quality of wine seems to be reaching certain limits we decide that perhaps another technique is more appropriate to the dataset at hand.

The next idea was to use a multi-class classification model with pytorch again. The 11 features were used. The model consisted of 3 layers of perceptrons. Several variables to the model such as 'epochs', 'batch_size', 'learning_rate', and 'amount of perceptrons' in each layer was adjusted to try and achieve the best score possible. Unfortunately, after much tinkering with the model, an accuracy score of 46% was achieved. We can clearly see that our model overfits consistently and we need to find a way to reduce the overfitting and increase the accuracy.


Installation 

![Installation package](DL-wine-quality/packagelist.txt)
