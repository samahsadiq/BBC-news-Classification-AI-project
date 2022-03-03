# BBC-news-Classification-AI-project
The aim of the model is to classify a BBC article into its category which is one of the 5 categories (business, entertainment, politics, sport, tech). The given input were a BBC folder which consists of 2225 documents from the BBC news website corresponding to stories in five topical areas from 2004-2005.

To access the data, the bbc folder should be uploaded into Google Drive. Using Google Colab, you needed to grant the access and copy the link of the bbc folder and paste it into the code in the (bbc_path) variable. The code should be able to navigate through the categories folders and extract the data.

There some chats provided for the data to be easier for understanding. 

Some preprocessing techniques were used to clean the data from (stop-words, numbers, non-english words, punctuation, unnecessary spaces, new lines and uppercase).

The names of the categories have mapped to numbers for labeling. 

The preprocessed full dataset is divided into Training set (80%), Development set (10%), and Testing set (10%).

Some features extractions techniques were used like words freaquancy, n-grams, TFidfVectorizer.

For Features selection methods, the “SelectKBest” and “chi2” were used to select only the most important number of features. A couple of number of features were examined on the Development set (k=500, 700, 1000, 2000, 2553). 

For the sake of experiment, I have trained 4 different classifiers and picked the best one performed well on development set based on the accuracy. The chosen classifiers are:Support Vector Machine (SVM), Random Forest (RF), Logistic Regression (LR), Decision Tree (DT).

After training each model, they were tested on the Development set. The best 2 models were the SVM and the (LR) with up to 97%. However, the (LR) was selected because it has a fewer enhancement in the f1-scores.

As I selected the Logistic Regression based on its accuracy on the Development set, it has been tested on the Test set and achieved up to 98% which is considered as a very good accuracy.
