# Titanic-Survival-Prediction-Linear-Regression
## Task:
Build a machine learning model that predicts which passengers survived the Titanic shipwreck.</br>
Comes under **Supervised Learning** as Labelled data is provided.</br>
**Logistic Regression** algorithm is used to achieve the result.</br>
Tools Used: Jupyter Notebook, Python

## Dataset:
The dataset is taken from Kaggle's "Titanic - Machine Learning from Disaster". The dataset contains 891 records and 12 features. The features are:
- PassengerId
- Survival: Passenger Survived or not,	0 = No, 1 = Yes
- Pclass: Ticket class,	1 = 1st, 2 = 2nd, 3 = 3rd
- Name
- Sex: Male or Female	
- Age: Age in years and float value	
- Sibsp: Number of Siblings or Spouses on Titanic
- Parch: Number of Children or Parents on Titanic
- Ticket:	Ticket number	
- Fare:	Passenger fare	
- Cabin:	Cabin number	
- Embarked:	Port from where passengers got on Titanic,	C = Cherbourg, Q = Queenstown, S = Southampton</br></br>
Source: https://www.kaggle.com/competitions/titanic/data

## Steps Involved:
### Import Dependencies:
Libraries needed to implement the model are:

- NumPy
- Pandas
- Matplotlib.Pyplot
- Seaborn
- train_test_Split from sklearn.model_selection
- Logistic Regression from sklearn.linear_model
- accuracy_score from sklearn.metrics

### Data Collection and Analysis:
- Load the data using read_csv function from pandas
- Used functions shape, head, info and describe to know more about data.
- Check for missing value

### Data Preprocessing:
- Handling the missing value
  1. Dropped the column cabin from the data frame as it has more than half of the missing values
  2. Replaced the missing values of Age with the mean value of the Age column
  3. Replaced the missing values of Embarked with the mode value of the Embarked column
- Encoding the Categorical Columns
  1. Replace the Sex column data as 0(Male) and 1(Female)
  2. Replace the Embarked column data as 0(S), 1(C) and 2(Q)
- Split the data into Features and Target.
  1. Features: Pclass, Sex, Age, SibSp, Parch, Fare, Embarked
  2. Target: Survived
### Data Visualization
- Used Seaborn to plot the graph
- Count Plot for each feature
- Count Plot tp compare one feature to another
### Model Building
- Splitting the data into training and test data: 20% for testing and 80% for training
- Model Training: Used **Logistics Regression** which used Sig,oid function to extract the result
- Model Evaluation: Done on both Training and test data
  1. Accuracy Score for Trained data:  0.8075842696629213
  2. Accuracy Score for Test data:  0.7821229050279329
### Build a Predictive System:
- Take random data from the dataset
- Convert it to numpy array then further reshape it into 2D array
- Predict the result using the designed model
- Print the result.</br></br></br>
Reference: Project 15. Titanic Survival Prediction using Machine Learning in Python | Machine Learning Project, Siddhardhan, https://www.youtube.com/watch?v=Lgp14y9-U74&list=PLfFghEzKVmjvuSA67LszN1dZ-Dd_pkus6&index=15
