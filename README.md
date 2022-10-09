# Neural Network Charity Analysis
*Deep Learning ML*

## Project Overview
For this project, we are going to **Neural Networks Machine Learning algorithms**, also known as artificial neural networks, or ANN. For coding, We are using Python  **TensorFlow** library in order to create a binary classifier that is capable of predicting whether applicants will be successful if funded by nonprofit foundation *Alphabet Soup*.
This ML model will help ensure that the foundation’s money is being used effectively. With neural networks ML algorithms we are creating a robust deep learning neural network capable of interpreting large complex datasets. Important steps in neural networks ML algorithms are data cleaning and data preprocessing as well as deciding what data is beneficial for the model accuraccy.

## Purpose

With knowledge of machine learning and neural networks, create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, we received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization.

With the help of Pandas knowledge and the Scikit-Learn’s StandardScaler(), we need to preprocess the dataset in order to compile, train, and evaluate the neural network model

## Requirements
- Preprocessing Data for a Neural Network Model
- Compile, Train, and Evaluate the Model
- Optimize the Model
- A Written Report on the Neural Network Model


## Resources
-	Dataset [charity_data.csv](Resources/charity_data.csv)
-	Software: **Jupyter Notebook**
-	Languages: **Python**
-	Libraries: **Scikit-learn**, **TensorFlow**, **Pandas**
-	Environment: **Python 3.7**



## Results 

### Data Preprocessing

**What variable(s) are considered the target(s) for your model?**

- “IS_SUCCESSFULL” column is the target.
- Target variables are also known as dependent variable and we are using this variable to train our ML model.

**What variable(s) are considered to be the features for your model?**

- Variables include all columns, except target variable and the one(s) we dropped “EIN" and "NAME” in the first trial and “EIN” in optimization trial.
- Input values are also known as independent variables, and are considered to be features for the model.

**What variable(s) are neither targets nor features, and should be removed from the input data?**

- The variables that should be removed and are neither targets nor features are variables that are meaningless for the model. 
- The variables that don’t add to the accuracy to the model. One of the examples would be variables with all unique values. 
- Another thing to keep in mind is to take care of the Noisy data and outliers. 
- We can approach this by dropping outliers or by bucketing. 

### Compiling, Training, and Evaluating the Model

**How many neurons, layers, and activation functions did you select for your neural network model, and why?**

- We used 2 layers, because 3 layers didn’t contribute much to the improvement of the ML module. 
- This is because the additional layer was redundant—the complexity of the dataset was encapsulated within the two hidden layers. 
- Adding layers does not always guarantee better model performance and depending on the complexity of the input data, adding more hidden layers will only increase the chance of overfitting the training data.
- Here we used **relu** activation function, since it has the best accuracy for this model.
- 200 neurons for the first layer and 90 neurons for the second layer. 
- As recommended the first layer should have at least double the amount of input features, that is 100 input values (rows) in our case.
- **adam** optimizer, which uses a gradient descent approach to ensure that the algorithm will not get stuck on weaker classifying variables and features and to enhance the performance of classification neural network.
- As for the loss function, **binary crossentropy** comes in the picture, because it is specifically designed to evaluate a binary classification model.
- The model was trained on 500 epochs, tried to increase from 200 epochs because the model improved a bit, however, it did not increase for too many epochs in order to avoid overfitting. 


![Neural_Network_Charity_Analysis](https://github.com/Lauramasonjar/Neural_Network_Charity_Analysis/blob/main/Images/Defining_a_model.png)
<p align="center">
<i>Figure 1: Defining a Model.</i>
</p>

**Were you able to achieve the target model performance?**

- Yes. After a few configurations we achieved the target model performance.
- The model accuracy improved to 76.16%. Figures below show the accuracy score after optimization at 76.15% and before optimization at 72.57%.


![Neural_Network_Charity_Analysis](https://github.com/Lauramasonjar/Neural_Network_Charity_Analysis/blob/main/Images/accuracy_after.png)
<p align="left">
<i>Figure 2: Accuracy After Optimization.</i>
</p>


![Neural_Network_Charity_Analysis](https://github.com/Lauramasonjar/Neural_Network_Charity_Analysis/blob/main/Images/accuracy_before.png)
<p align="left">
<i>Figure 3: Accuracy Before Optimization.</i>
</p>



**What steps did you take to try and increase model performance?**

To increase model performance, the following steps were taken:

-	Checked input data and brought back **NAME** column that was initially skipped. 
- Set a condition on the values that are less than 50 in “Other” group. That reduced the number of unique categorical values by binning the values.
-	Binned the **ASK_AMT** values.
-	Initially the third layer was added with 40 neurons, however, it was changed back to 2 layers because the results did not improve much at all. 
-	Increased neurons for each layer (200 for 1st, 90 for 2nd).
-	Increased Epochs to 200.

## Summary

***Summary of the results***

- The model loss and accuracy score tell us how well the model does with the dataset and parameters that we used to build the model.
- Loss score is equal to 0.5996, meaning the probability model to fail is 59.96% and accuracy score is 0.7615, meaning that the probability model to be accurate is 76.15%.

***Recommendation for further analysis***

- After some fine-tuning the model reached an accuracy score of 59.96%.
- Although the model reached the required criteria it might not be the best model for this dataset. 
- The loss score for that model is still about 60%, what is quite high. 
- The dataset that we were working with seemed to be a good fit because of the length of the dataset and its complexity, even though the results weren't the best. Adding new input values seemed a good choice when improving the model accuracy. 
- In this case I would consider adding more input values (if they are available in the original dataset, for example). We could also consider gathering more data.
-  Although gathering more data is not always the easiest decision it is sometimes necessary.
