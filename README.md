# Decesion-Trees-Titanic-Project

## Project Overview
This project involves building a Decision Tree classifier to predict Titanic passenger survival. The model is initially trained without depth restrictions, visualised, and its accuracy is evaluated on the development set. Then, models with different max_depth values (2-10) are trained, visualised, and their accuracies on training and development sets are plotted. The best model is then tested, and its accuracy on the test set is reported.

## Technologies Used
1) Python
2) Pandas
3) NumPy
4) Scikit-Learn
5) Matplotlib

## Dataset
The dataset used for this project is 'titanic.csv', which contains information about Titanic passengers.

# Project structure
```markdown
decision-trees-titanic/
│
├── data/
│   └── titanic.csv
│
├── notebook/
│   └── decision_trees_titanic.ipynb
│
├── results/
│   ├── bagging_classifier_tree.png
│   ├── random_forest_classifier_tree.png
│   └── adaboost_classifier_tree.png
│
└── requirements.txt
```

## Methodology
1) Data Collection:
   
   The project uses the public 'titanic.csv' dataset, which includes information about passengers on the Titanic. This dataset contains various features such as age, sex, passenger class, fare, and whether the passenger survived or not.

2) Data Preprocessing:
   1. Loading the Data: the dataset is loaded using Pandas, a data manipulation library in Python.
   2. Handling Missing Values: missing values are addressed by filling them with the median value.
   3. Encoding Categorical Variables: Converting the categorical variable 'Sex' into numerical values using techniques like one-hot encoding to make them suitable for the machine learning model.

3) Feature Engineering:
   
   Features such as 'Name', 'PassengerId', 'Ticket', and 'Embarked' are removed as they do not contribute significantly to the model's performance.
      
5) Exploratory Data Analysis (EDA):
   1. Statistical Analysis: Descriptive statistics are computed to understand the data types and distribution and of the data.
   2. Data Visualisation: Visual tools such as histograms, scatterplots are used to identify patterns, correlations, and insights within the variables.

6) Model Building and Training:
   1. Splitting the data into training and testing sets (75-25 split).
   2. Bagging Classifier: Uses multiple instances of a decision tree classifier to reduce variance.
   3. Random Forest Classifier: An ensemble of decision trees that improves prediction accuracy and controls overfitting.
   4. AdaBoost Classifier: Combines multiple weak classifiers to create a strong classifier.
   5. Visualisation: Trees from the Bagging, Random Forest, and AdaBoost classifiers are visualized and saved as images to understand the decision-making process of each model.
      
7) Model Evaluation:
   
   Accuracy Evaluation: The accuracy of each model is evaluated on the training and development sets to compare their performances.
   
8) Hyperparameter Tuning:
   1. Parameter Grid Definition: A grid of parameters for n_estimators and max_depth is defined.
   2. Grid Search with Cross-Validation: GridSearchCV is used to find the optimal number of estimators and maximum depth for the Random Forest model, using accuracy as the scoring metric.

9) Best Model Selection and Final Evaluation:
   1. Best Parameters Identification: The best parameters obtained from GridSearchCV are used to retrain the Random Forest model.
   2. Final Accuracy Calculation: The accuracy of the retrained Random Forest model is calculated and compared with the other models to determine the best-performing model.

## Setup and installation
1) Clone the repository:
   ```bash
   git clone https://github.com/ellahu1001/decision-tree-titanic.git
   cd decision-tree-titanic
   ```
2) Install the required packages:
   ```bash
   pip install -r Requirements.txt
   ```
3) Run the Jupyter Notebook:
   ```bash
   jupyter notebook notebook/Decision_Tree_Titanic.ipynb
   ```
   
## Requirements
The 'Requirements.txt' file lists all the Python packages required to run the project. Install these dependencies to avoid any compatibility issues.

## Results
1) Best parameters: max_depth = 10, n_estimators: 100
2) The accuracy score for the bagged classifier is: 0.767
3) The accuracy score for the randome forest classifier is: 0.785
4) The accuracy score for the boosted classifier is: 0.807
5) The accuracy score for the random forest classifier with the best parameters is: 0.812
6) The visualisation of the trees from Bagging, Random Forest, and AdaBoost classifiers are attached.

## Conclusion 
According to the accuracy scores calculated, the model with the highest accuracy score, hence, the model that performed the best is the tuned random forest classifier model, with the values n_estimators=100 and max_depth=10.
