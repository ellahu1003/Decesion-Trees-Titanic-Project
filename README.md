# Decesion-trees-titanic

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

## Setup and installation
1) Clone the repository:
   ```bash
   git clone https://github.com/ellahu1001/decision-tree-titanic.git
   cd decision-tree-titanic
   ```
2) Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```
3) Run the Jupyter Notebook:
   ```bash
   jupyter notebook notebook/Decision_Tree_Titanic.ipynb
   ```
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
## Requirements
The 'requirements.txt' file lists all the Python packages required to run the project. Install these dependencies to avoid any compatibility issues.

## Results
1) Best parameters: max_depth = 10, n_estimators: 100
2) The accuracy score for the bagged classifier is: 0.767
3) The accuracy score for the randome forest classifier is: 0.785
4) The accuracy score for the boosted classifier is: 0.807
5) The accuracy score for the random forest classifier with the best parameters is: 0.812
6) The visualisation of the trees from Bagging, Random Forest, and AdaBoost classifiers are available in the results folder.

## Conclusion 
According to the accuracy scores calculated, the model with the highest accuracy score, hence, the model that performed the best is the tuned random forest classifier model, with the values n_estimators=100 and max_depth=10.
