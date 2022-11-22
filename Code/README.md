COMP30027 Assignment 2 README

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Submission zip file Content
5 CSV file for predicted result of test dataset delivered by 5 Models for Kaggle submission
1 Jupyter Notebook for running the code
1 PNG for correlation heat map
1 PNG for boxplot
1 txt type group file for storing group members information
1 txt type README file
1 md type README file

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Shorthand expression of Learners:

Multinomial Naive Bayes as "MNB"
Decision Tree as "DT"
Logistic Regression as "LR"
Support Vector Machine as "SVM"
Random Forest as "RF"
Stacking Model as "Stacking Model"

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Aim of the Coding Part:

Apply learners (MNB, DT, LR, SVM, RF, Stacking Model) on recipes instances (after preprocessing and feature engineering) to make the classification task on each recipes's cooking duration time (categorical)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Code of Importing Libraries (In Jupyter Notebook):
Run Cell 1 to import libraries

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Code for Exploring Data (In Jupyter Notebook):

Step 1 Read in Data
Run Cell 2 to read in all training and test datasets (raw data instances)

Step 2 Observe the Data
2.1 Run Cell 3 for having a printed out text of a overall observation of the training set

2.2 Run Cell 4 to get the correlation heat map between 'n_step' and 'duration_label', between 'n_ingredients' and 'duration_label' (A graph is rendered also a png picture is included in the submitted zip file)

2.3 Run Cell 4 to get boxplot of n_steps & duration_label and n_ingredients & duration_label (A graph is rendered also a png picture is included in the submitted zip file)

3.4 With the heat map and boxplot, features n_steps and n_ingredients from each feature shows weak correlation with the class labels (Not include them in the consideration of selected features)

2.5 Run Cell 5 & 6 to get the first 20 instances' steps feature content and first 50 instances ingredients feature content for presenting the provement of little correlation between n_steps and n_ingredients to the class label "duration_label"

Step 3 Remove Punctuations & Digits
Run Cell 7 to remove the punctuations and digits from text features "steps" and "ingredients" with regular expression

Step 4 Observe the word-appear-frequency with wordcloud
Run Cell 7 and create two wordcloud graph for better visualisation of investigating the most frequent appear words from features ingredients & steps (after removing the digits and punctuations)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Code for Preprocessing (In Jupyter Notebook):

Run Cell 8 for combining all text features of each instance from both training and test set, regular expression is applied on each combined feature to remove the punctuations and digits
This step delivers the combined feature of each instance as input for CountVectorizer() method in feature engineering step

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Code of Todense Method and Learning curve plot function (In Jupyter Notebook):

Step 1 Run Cell 9 to import the libraries

Step 2 Run Cell 10 to deploy the func DenseTransformer() which helps to convert the instance's TF-IDF value features into dense data for fitting model process
# The learning curve is already presented in the Report, by running this cell, it would takes long period of time to generate the plot (We mark this cell as comment type)

Step 3 Run Cell 11 to deploy the func plot_with_err() and func plot_learning_curve() which are applied by plotting the learning curve (with error) of each models we have build for classification task

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Code of LR with tuned parameters (In Jupyter Notebook):

Step 1 Run Cell 12 to present the validation score of the applied LR pipeline under cross-validation (notice that feature engineering methods including CountVectorizer(), tf-idf, select_K_Best and to_dense are all included in pipeline and are proceeded automatically before fitting and validating)

Step 2 Run Cell 13 to plot the learning curve of logistic regression model for visualisation of changing trend of training and validation score along with changing the training size
# The learning curve is already presented in the Report, by running this cell, it takes long period of time to generate the plot (We mark this cell as comment type)

Step 3 Run Cell 14 to generate the csv file containing the prediction result of test instance for submission to Kaggle

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Code of MNB with tuned parameters (In Jupyter Notebook):

Step 1 Run Cell 15 to present the validation score of the applied MNB pipeline under cross-validation (notice that feature engineering methods including CountVectorizer(), tf-idf, select_K_Best and to_dense are all included in pipeline and are proceeded automatically before fitting and validating)

Step 2 Run Cell 16 to plot the learning curve of MNB model for visualisation of changing trend of training and validation score along with changing the training size
# The learning curve is already presented in the Report, by running this cell, it takes long period of time to generate the plot (We mark this cell as comment type)

Step 3 Run Cell 17 to generate the csv file containing the prediction result of test instance for submission to Kaggle

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Code of DT with tuned parameters (In Jupyter Notebook):

Step 1 Run Cell 18 to present the validation score of the applied DT pipeline under cross-validation (notice that feature engineering methods including CountVectorizer(), tf-idf, select_K_Best and to_dense are all included in pipeline and are proceeded automatically before fitting and validating)

Step 2 Run Cell 19 to plot the learning curve of DT model for visualisation of changing trend of training and validation score along with changing the training size
# The learning curve is already presented in the Report, by running this cell, it takes long period of time to generate the plot (We mark this cell as comment type)

Step 3 Run Cell 20 to generate the csv file containing the prediction result of test instance for submission to Kaggle

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Code of SVM with tuned parameters (In Jupyter Notebook):

Step 1 Run Cell 21 to present the validation score of the applied SVM pipeline under cross-validation (notice that feature engineering methods including CountVectorizer(), tf-idf, select_K_Best and to_dense are all included in pipeline and are proceeded automatically before fitting and validating)

Step 2 Run Cell 22 to plot the learning curve of SVM model for visualisation of changing trend of training and validation score along with changing the training size
# The learning curve is already presented in the Report, by running this cell, it takes long period of time to generate the plot (We mark this cell as comment type)

Step 3 Run Cell 23 to generate the csv file containing the prediction result of test instance for submission to Kaggle

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Code of RF with tuned parameters (In Jupyter Notebook):
# Notice that this model's accuracy rate and learning curve is only used to comparison with Decision tree (no detail analysis is applied on this model)
# Notice that this model has to be run before the stacking model as it is one of the base models inside stacking method

Step 1 Run Cell 24 to present the validation score of the applied RF pipeline under cross-validation (notice that feature engineering methods including CountVectorizer(), tf-idf, select_K_Best and to_dense are all included in pipeline and are proceeded automatically before fitting and validating)

Step 2 Run Cell 25 to plot the learning curve of RF model for visualisation of changing trend of training and validation score along with changing the training size
# The learning curve is already presented in the Report, by running this cell, it takes long period of time to generate the plot (We mark this cell as comment type)

Step 3 Run Cell 26 to generate the csv file containing the prediction result of test instance for submission to Kaggle

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Code of Stacking Model with tuned parameters (In Jupyter Notebook):

Step 1 Run Cell 27 to present the validation score of the applied Stacking Model pipeline under cross-validation (notice that feature engineering methods including CountVectorizer(), tf-idf, select_K_Best and to_dense are all included in pipeline and are proceeded automatically before fitting and validating)

Step 2 Run Cell 28 to plot the learning curve of Stacking model for visualisation of changing trend of training and validation score along with changing the training size
# The learning curve is already presented in the Report, by running this cell, it takes long period of time to generate the plot (We mark this cell as comment type)

Step 2 Run Cell 29 to generate the csv file containing the prediction result of test instance for submission to Kaggle