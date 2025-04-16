# 6 step field guide for building machine learning

source: https://www.mrdbourke.com/a-6-step-field-guide-for-building-machine-learning-projects/
![alt text](<Screenshot (74).png>)

# 1st step: types of machine learning problem

To help decide whether or not your business could use machine learning, the first step is to match the business problem you’re trying to solve a machine learning problem.

1) **Supervised Learning** is called supervised because you have data and labels. A machine learning algorithm tries to learn what patterns in the data lead to the labels. The supervised part happens during training. If the algorithm guesses a wrong label, it tries to correct itself.

Two main type of supervised learning

1.1) **Classification**: predicting if something is one thing or another?

- Binary classification = two options such as if you want to predict that patient had heart disease or not based on their medical records.

- Multi-class classification = more than two options such as what type of dog breeds in this image.

1.2) **Regression** involves try to predict a number such as how much with this house sell for based on things like number of rooms, the area it's in.


2) **Unsupervised Learning** is when you have data but no labels. The data could be the purchase history of your online video game store customers. Using this data, you may want to group similar customers together so you can offer them specialised deals. You could use a machine learning algorithm to group your customers by purchase history.

After inspecting the groups, you provide the labels. There may be a group interested in computer games, another group who prefer console games and another which only buy discounted older games. This is called clustering.

3) **Transfer Learning**

Transfer learning is when you take the information an existing machine learning model has learned and adjust it to your own problem.

Training a machine learning model from scratch can be expensive and time-consuming. The good news is, you don’t always have to. When machine learning algorithms find patterns in one kind of data, these patterns can be used in another type of data.

4) **Reinforcement Learning**

# 2nd step: types of data

1) Structured data — Think a table of rows and columns, an Excel spreadsheet of customer transactions, a database of patient records. Columns can be numerical, such as average heart rate, categorical, such as sex, or ordinal, such as chest pain intensity.

2) Unstructured data — Anything not immediately able to be put into row and column format, images, audio files, natural language text.

3) Static data — Existing historical data which is unlikely to change. Your companies customer purchase history is a good example.

4) Streaming data — Data which is constantly updated, older records may be changed, newer records are constantly being added.

# 3rd step: Evaluation — What defines success?

Example: A 95% accurate model may sound pretty good for predicting who’s at fault in an insurance claim. But for predicting heart disease, you’ll likely want better results.

# 4th step: What features does your data have and which can you use to build your model?

Features are referring to different kinds of data within data.

The three main types of features are categorical, continuous (or numerical) and derived.

1) **Categorical features** — One or the other(s). For example, in our heart disease problem, the sex of the patient. Or for an online store, whether or not someone has made a purchase or not.

2) **Continuous (or numerical) features** — A numerical value such as average heart rate or the number of times logged in.

3) **Derived features** — Features you create from the data. Often referred to as feature engineering. Feature engineering is how a subject matter expert takes their knowledge and encodes it into the data. You might combine the number of times logged in with timestamps to make a feature called time since last login. Or turn dates from numbers into “is a weekday (yes)” and “is a weekday (no)”.

# fifth step: modelling. Which model should you choose? How can you improve it? How do you compare it with other models?

Important concept:

![alt text](<Screenshot (75).png>)

Three parts:

![alt text](<Screenshot (76).png>)

1) **choosing a model**

When choosing a model, you’ll want to take into consideration, interpretability and ease to debug, amount of data, training and prediction limitations.

- Interpretability and ease to debug — Why did a model make a decision it made? How can the errors be fixed?

- Amount of data — How much data do you have? Will this change?

- Training and prediction limitations — This ties in with the above, how much time and resources do you have for training and prediction?

To address these, start simple. A state of the art model can be tempting to reach for. But if it requires 10x the compute resources to train and prediction times are 5x longer for a 2% boost in your evaluation metric, it might not be the best choice.

Linear models such as logistic regression are usually easier to interpret, are very fast for training and predict faster than deeper models such as neural networks.

2) **Tuning a model**

A model's first results isn’t its last. Like tuning a car, machine learning models can be tuned to improve performance.


Things to remember: 

- Machine learning models have hyperparameters you can adjust. Such as number of trees for random forests and number of and type of layers for neural networks. 

- A models first results aren't its last 

- Tuning can take place on training or validation data sets.

3) **Comparing models**

- Underfitting mean model is too simple that it cannot reflect the complexity of the training dataset.

fixes: increase the complexity of the model or training the model for a longer period of time to reduce an error.

- Overfitting mean when your model memorizes all the specific details of training data and fails to generalize. It tends to perform bery well on some traning dataset but poorly on any new training dataset.

fixes: collect more data, try a less advanced model.

Things to remember: 

- Want to avoid overfitting and underfittinhg.
- keep the test set eparate at all costs.


![alt text](<Screenshot (77).png>)


# sixth step: Experiments