# Similarity_in_Quora_Question
In this project, we examine the problem of text similarity to get rid of the same questions asked over the question-and-answer platform known as ‘Quora’. Typical text contents encountered in real applications are massive and what makes it huge is the redundancy of the content over the internet. We design a systematic way to find out the text-similarity between n questions using several models such as Linear Support Vector Machine (SVM), Logistic Regression, XG-Boost model.
DOCUMENTATION OF CODE
➢ Introduction:
o We are working on the dataset of Quora question text similarity problem. We have used various methods for feature extraction, preprocessing of dataset, dimensionality reduction and evaluating on model.
o We have implemented models like Logistic regression, Linear SVM and XgBoost.
➢ We have written code for evaluating the text similarity on the dataset obtained from the Quora repository.
➢ The dataset can be downloaded from the following link:
o http://qim.fs.quoracdn.net/quora_duplicate_questions.tsv
➢ Read the dataset and analyze it.
➢ Filled the null value with ‘1’ in dataset.
➢ To make the model robust and very effective, calculated features before and after the preprocessing of dataset.
➢ Analyzed all the features.
➢ For extracting features, we need to split the sentence, for which we have used token.
➢ In preprocessing, stopwords are also removed using nltk.
➢ Plot the word cloud graph to understand our dataset better.
For Duplicate pair of question:
For Non-Duplicate pair of question:
➢ Used TSNE for analyzing high dimensional data and converting them into lower dimension data (both 2D and 3D)
➢ Added all the basic and advance features in one file and remove all the null values from dataset.
➢ Now the dataset of just features looks like:
➢ Calculated TF-IDF vectorizer on both the columns ‘question1’ and ‘question2’ for the further training and testing purpose.
➢ Then split the dataset into train and test set in the ration of 70:30.
➢ Imported all the libraries required for the evaluation of final model.
➢ At first, we implemented logistic regression and calculated the log loss for different values of alpha as mentioned in the figure below.
Calculating the value of log loss for different value of alpha:
Plotting the graph “cross validation error”
The best value of log loss for train and test set for the best alpha value:
➢ Then we implemented linear SVM and calculated the log loss for different values of alpha as mentioned in the figure below:
Calculating the value of log loss for different value of alpha:
Plotting the graph “cross validation error”
The best value of log loss for train and test set for the best alpha value:
➢ The main difference between the logistic regression and linear SVM is that both uses different loss function. One uses ‘log’ and another uses ‘hinge’.
➢ The third and final model we implemented is XgBoost.
➢ As we have performed first linear SVM and logistic regression, hence we have called the file features file once again for XgBoost and performed necessary steps along with the train and test split steps again.
➢ The log loss calculated is as shown in the figure below:
➢ Things worked and didn’t worked:
o Using our best knowledge, we were able to implement everything with some decent challenges and some tough ones too.
o One of the tough was to implement XgBoost, as we have to calculate vectors, which use trained GLOVE model (which is trained on Wikipedia). It caused the dimension problem in matrix, which was solved later by the guidance of professor and some online sources. But as it is too long to calculate, sometimes the session does timeout for long running.
