##### Compilation of Python programming code of various AI and Machine Learning projects using Convolutional Neural Networks, Artificial Neural Networks, Supervised Learning models - Linear Regression, Logistic Regression, Decision Tree, Random forest, Bagging Classifier, AdaBoost, Gradient Boosting and XGBoost. 
| Project                            |Description                                                                                       |Jupyter Notebook Link     
:-----------------------------------:|------------------------------------------------------                                            |:--------------------
|<img width=200/>|<img width=500/>|
| Twitter Sentiment Classification using NLP | <p align="justify">* To classify the sentiment of positive, negative, and neutral tweets, about problems of each major U.S. airline. </p> <p align="justify">* Firstly, performed EDA and inferred that Majority of the tweets are negative (63%), followed by neutral tweets (21%), and then the positive tweets (16%) and Virgin airlines is the only airline where the ratio of the three sentiments is somewhat similar. Visualized the word cloud of the Negative and Positive tweets to filter the most frequent tweet words. </p> <p align="justify">* Preprocessed the text with steps: 1) Remove html tags 2) Replace contractions in string. (e.g. replace I'm --> I am) and so on. 3) Remove numbers 4) Used NLTK library to tokenize words , remove stopwords and lemmatize the remaining words. </p> <p align="justify">* Preprocessed the text into numbers using CountVectorizer (bag of words) and built a Random Forest classifier model using 10 estimators. Measured cross_validation_score=71%. </p> <p align="justify">* Tuned the model to accuracy increased to 76% with optimal number of base learners (optimal number of base learners corresponds to minimum misclassification error) obtained using K-Fold Cross Validation and evaluated the model prediction on test data and visualizing it on confusion matrix. </p> <p align="justify">* Used another technique caled TF-IDF(Term Frequency(TF) - Inverse Document Frequency(IDF)) to preprocess the text and built Random Forest classifier model. Evaluated the model performance, then tuned for optimal number of base learners that improved the model performance to 76% accuracy. Visulized the tuned model performance using confusion Matrix  </p> | https://github.com/sandhyakaranam/Machine-Learing-Projects/blob/main/NLP_Twitter_Sentiment_Classification.ipynb    |
| Plant Seedlings Classification using CNN | <p align="justify">* The dataset contain images of unique plants belonging to 12 different species. Used **deep learning model** to classify plant seedlings.  </p> <p align="justify">* Preprocessed the Images with steps: 1) Converting RGB Images int HSV (In this problem, color is an important factor in identifying the plant species. Hence converting BGR TO HSV is a good idea) 2) Used Gaussian Blurring to remove noise 3) Create mask to remove background 4) Normalizing the images  </p> <p align="justify">* Built a **Convolutional Neural Network**  model using 6 Conv2D layers followed by 2 dense layers, categorical_crossentropy loss function, RMSprop optimizer. </p> <p align="justify">* Plotting Training and Validation accuracy showed overfitting model after 35th epoch. So, reduced the overfitting of the model using 2 Techniques: 1) reducing the _learning rate_ 2) Data Augmentation (Regularization)  </p> <p align="justify">* With learning_rate-reduction and data augmentation, obtained more generalized model, generalizing well to the validation set and improving model accuracy on test data to 86% </p> <p align="justify">* The optimised model gives better prediction, almost by 87% accuracy as seen from the confusion matrix. </p> <p align="justify">* The model accuracy becomes constant after the 25th epoch, reducing learning rate worked well and Data Augmentation worked as a regularizer and helped to reduce the variance in the training and increasing the generalization of the model. </p> | https://github.com/sandhyakaranam/Machine-Learing-Projects/blob/main/Computer%20Vision_Plant_Seedlings_Classification.ipynb     |
| Bank Customer Churn Prediction using ANN- To help the operations team identify the bank customers that are more likely to churn    | <p align="justify">* Built a **Deep neural Network**  model using _Tensor flow_ and _Keras_ with 4 hidden layers, binary_crossentropy loss function, Adam optimizer. </p> <p align="justify">* Optimized the model using Grid Search CV for 2 hyperparameters _batch_ size and _epochs_ and reduced overfitting using _dropout_ and early stopping. </p> <p align="justify">* The model's validation loss curve did not have high slope, so optimized further using roc-curve optimal threshold  that improved model performance with a recall of 73% reducing the false negatives and increasing the True positives. </p> <p align="justify">* The optimised model gives better prediction as seen from the confusion matrix as well as improved accuracy. </p> <p align="justify">* Based on the insights from the EDA we can conclude that the older, female and inactive customers have greater churn rate.</p> | https://github.com/sandhyakaranam/Machine-Learing-Projects/blob/main/Bank_Churn_Prediction_using_ANN.ipynb      |
| Credit Card Customer Segmentation using Clustering models  | <p align="justify">* Analyzed data through **Statistical Analysis** and **Exploratory data Analysis** (bar, histogram and box plots) to draw relationship patterns and correlation between variables to draw insights.</p> <p align="justify">* Performed bi-variant analysis using Pair plot and heat map to understand correlation between the features. </p> <p align="justify">* Preprocessed the data like detection outliers using z-score, so they can form their own cluster. Also, scaled the data using Standard Scaler and fit the **K-Means Clustering** model on it. </p> <p align="justify">* Measured the optimal number of clusters, K=3 for building K-Means clustering model, using Elbow method from the plot of Average Distortion Vs Number of K-Means clusters. </p> <p align="justify">* Evaluated the quality of K-Means clusters in terms of how well samples are clustered with other samples that are similar to each other using Sihouette scores of K-Elbow Visualizer and for K=3 obtained the highest Sihouette score of 0.93. </p> <p align="justify">* Even measured optimal number of clusters with Silhouette coefficients (Silhouette Visualizer) and confirmed number of K-Means clusters=3. </p> <p align="justify">* Did customer segmentation using K-means clustering for 3 clusters. </p> <p align="justify">* Performed **Hierarchical Clustering** for difference distance metrics (like ["euclidean", "chebyshev", "mahalanobis", "cityblock"]) and different Linkage methods (like ["single", "complete", "average", "weighted"]) and measured Cophentic Correlation for different combinations of distnace metrics and Linkage methods. Highest cophenetic correlation is 0.89 obtained with Euclidean distance and average linkage. </p> <p align="justify">* For each Linkage method, plotted Dendograms and Dendrogram with average linkage shows distinct and separate cluster tree. </p> <p align="justify">* Performed customer segmentation using Hierarchical Clustering (also called Agglomerative Clustering) for no. of clusters, k=3, average Linkage method and Euclidean Distance. </p> <p align="justify">* Compared  Cluster profiling for K-Means clustering Vs Hierarchical Clustering. Both these Clustering techniques gave similar segments. </p> <p align="justify">* Drew Insights from the 3 clusters for business recommendations. Using Proncipal Component Analysis, experimented reducing the dimensions to 2  to see how well-separated the clusters are .</p> | https://github.com/sandhyakaranam/Machine-Learing-Projects/blob/main/USL_Project_CreditCardCustomerSegmentation.ipynb  |   
| AllLifeBank Personal Loan Campaign Modelling   |  <p align="justify">* Built **Logistic Regression and Decision Tree** predictive models, that the bank can deploy to identify potential customers who will be interested in taking a personal loan and that the bank can use to find the key factors that will have an impact on a customer taking a personal loan or not.</p> <p align="justify">* Built Logistic Regression model with optimal threshold using _AUC-ROC curve_ that gave a  _recall_ of 0.85 on Test data. Also, built this model with optimal threshold using _Precision-Recall curve_, that will help the bank to maintain a balance in identifying potential customer and the cost of resources, with _F1-score_ of 0.75 on Test data.</p> <p align="justify">* Built **Decision Tree** default model and tried hyper tuning the model using _Pre-pruning_ and _Cost complexity pruning_. However, on this dataset, although the tree became much simpler and readable with pruning, Decision Tree default model gave best performance compared to hyper tuned models. </p> <p>* Overall, on this dataset, Decision Tree model gives best recall of 0.93 on the test data, compared to Logistic Regression model.</p> <p align="justify">* Looking at important variables based on _p-values_ in Logistic regression and _Feature importance_ in Visualized Decision trees, found the key factors that have an impact on Personal Loan.</p> | https://github.com/sandhyakaranam/Data-Science-Projects/blob/main/SLC_LR_DT%20-%20Bank%20Personal%20Loan%20Campaign.ipynb       |
| Credit Card Churn Prediction using Ensembled models  | <p align="justify">* Analyzed data through **Statistical Analysis** and **Exploratory data Analysis** to draw relationship patterns and correlation between variables to draw insights.</p> <p align="justify">* Split the dataset into train, Validation and test sets and performed _Feature Engineering_ on Train and Validation data like missing value imputation using _SimpleImputer_ and encoding categorical variables using _one-hot encoder_.</p> <p align="justify">* Built and Trained different classification models: **Logistic Regression, Bagging Classifier, Random Forest, Gradient Boosting, AdaBoost, XGBoost and Decision Tree** with original data, with over sampled  data (using _SMOTE_) and with under sampled data (using _RandomUnderSampler_).</p> <p align="justify">* Analyzed all 6 models prediction accuracy using _K-Fold cross-validation score_ and _recall_ score and picked the 3 best performance models : Gradient Boosting, AdaBoost and XGBoost with original and under sampled data.</p> <p align="justify">* Hyper Tuned these 3 best models with under sampled data and original data and compared the model performance. Gradient Boosting with original data gave more generalized performance on test data.</p> <p align="justify">* Built the final **Pipeline** model with the best parameters obtained for Gradient Boosting classification model, that the bank can deploy to identify customers who are at the risk of Attrition.</p> | https://github.com/sandhyakaranam/Data-Science-Projects/blob/main/Hyper%20Tuning%20and%20Pipeline%20-%20Credit%20Card%20Churn%20Prediction.ipynb  |
| Cars4U - Tech start-up that aims to find foothold in the used car market     | <p align="justify">* Built a **Linear Regression** predictive model with Python Library _SciKit-Learn_, that can effectively predict within ~13% of the used car price (using metric _MAPE_) and can explain variance in the used car price up to 94% (using metric _R-squared_). </p> <p align="justify">* From the baseline model, improved complexity of the model by reducing to one third of the features using _Sequential Feature Selector_ (SFS) and obtained similar model performance, that can effectively predict within ~14% of the used car price and can explain variance in the used car price up to 90%. </p> <p align="justify">* Through EDA, generated insights and recommendations, to help business in devising profitable strategies using differential pricing.</p> | https://github.com/sandhyakaranam/Data-Science-Projects/blob/main/SLR_Cars4U%20Pricing%20Model.ipynb      |
| Cardio Fitness Product Analysis  | <p align="justify">* Through **Statistical analysis** using Python Libraries _Numpy and Pandas_, analyzed which of the various cardio fitness products is effective in terms of fitness and usage.</p> <p align="justify">* Performed **Exploratory Data Analysis** (EDA) through **data visualization** (univariate and multi-variate analysis) using Python Library _Seaborn_, to draw relationship patterns and correlation between features to build customer profile of the different fitness products. Generated a set of insights & recommendations that will help the company in targeting new customers.</p>| https://github.com/sandhyakaranam/Data-Science-Projects/blob/main/Cardio%20Good%20Fitness-EDA.ipynb    |

