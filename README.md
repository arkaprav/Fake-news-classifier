# Fake news classifier
In this project, we have collected the dataset from kaggle.com. we have cleaned the data and transferred the text data into usable data by using stemming and one_hot vectorizer. After transformation we used padding for symmetry of the features.
## First model
We built a model using an embedding layer at first, followed by a LSTM layer of 100 neurons density, followed by a dense layer with sigmoid activation for classified output. Then the model is trained for 10 epoches.
### results:
192/192 [========================] - 6s 32ms/step - loss: 0.0021 - accuracy: 0.9997 - val_loss: 0.6474 - val_accuracy: 0.9145
The report says the after training the training accuracy is 0.9997 and the validation accuracy is 0.9145 which is very good results.
The confusion matrix for this prediction test results on test data is - 
[[3096,  323],
[ 193, 2423]]
## Second model
We built a model using an embedding layer at first, followed by a dropout layer of dropout ratio 0.3, followed by a LSTM layer of 100 neurons density, followed by a dropout layer of dropout ratio 0.3, followed by a dense layer with sigmoid activation for classified output. Then the model is trained for 10 epoches.
### results:
192/192 [========================] - 6s 32ms/step - loss: 0.0177 - accuracy: 0.9937 - val_loss: 0.3978 - val_accuracy: 0.9102
The report says the after training the training accuracy is 0.9937 and the validation accuracy is 0.9102 which is a poor result than the previous one.
The confusion matrix for this prediction test results on test data is - 
[[3105,  314],
[ 228, 2388]]
## Conclusion
From the above results we can definitely say that the first model is best for this problem, but for a huge dataset with so many features, the dropout layer will be more efficient than the singular layer of lstm.
