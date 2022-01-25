# Introducing-xG-Premium- 
DBA5106 Term Project. Improving on publicly available non-Penalty Expected Goals (npxG) data. But for brevity, xG is used throughout

#### Techniques Employed
EDA, Feature Engineering, Imbalanced Dataset, Hyper-parameter tuning (GridSearc, RandomSearch), Running & Evaluating Models (ROC-AUC) and Comparing metrics <br>

### Context
Football teams have been trying to find ways to score more goals in each game to win and to achieve better results in each season of their respective leagues. Traditionally, football teams have used past goals, shots, and shots on target to evaluate the goal-scoring ability of a player. However, recent trends show that more teams are using data analytics to find scientific approaches to evaluate a threatening player more objectively. Expected Goals (xG) measures the quality of goal-scoring chances by calculating the probability of scoring a goal from a given shot. This metric is not only
beneficial in determining how to score more goals, but it’s also important in developing teams’ tactics, positioning right players at the right area, and recruiting right players in the following season to achieve better results. <br>

### Dataset
The datasets used were from publicly avaiable data provided by StatsBomb <br>

### Implications & Insights
From initial pre-processing of data courtesy of **Sae Jin Jang's code (@saejin123)**, we feature engineered two more variables - distance to goal as well as shot angle from cosine rule.

Next, undersampling was done to tally up the counts of goals and no goals (since most shots do not result in a goal); Finally,
The following models were utilised in training and their metrics compared:
* Logistic Regression
* Decision Tree
* Linear Discriminant Analysis (LDA)
* K-Nearest Neighbors (KNN)
* Bagging (of Decision Tree)
* Random Forest
* Naive Bayes Gaussian (NB)
* Support Vector Machine (SVM)<br>

Top 3 performing models were:
* Random Forests
* SVM
* Logistic Regression

For Business use, we recommended logistic regression. The (slight) drop in accuracy & AUC score is offset by its greater interpretability vs Random Forests and not being as computationally expensive as SVM

###Credits 
Sae Jin's xG-Model-World-Cup-2018 <br>
Statsbomb. (n.d.). Statsbomb/open-data: Free football data from StatsBomb. GitHub. Retrieved November 12, 2021, from https://github.com/statsbomb/open-data.

### Collaborators
Sae Jin Jang (@saejin123)<br>
Hpone Myat Khine (@HponeMK) <br>
Kwanghun Lee (Jason) <br>
