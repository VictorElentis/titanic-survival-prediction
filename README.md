# Titanic Survival Prediction

Predicting Titanic passenger survival with logistic regression and random forest.

## Question
Can we predict whether a passenger survived using details like class, sex, age, and family size?

## What I did
- Explored the data and found that women and first-class passengers survived at much higher rates than men and third-class passengers.
- Cleaned missing values. I filled missing ages with the median age of passengers in the same class and sex, filled the 2 missing embarkation ports with the most common one, and dropped the deck column because most of it was missing.
- Created a family_size feature (siblings/spouses + parents/children + the passenger) and converted sex and embarkation port to numbers.
- Split the data 80/20 into training and test sets, keeping the survived/died ratio the same in both.
- Trained a logistic regression model as a baseline and a random forest to compare.

## Results
- Logistic regression: about 81% accuracy on the test set
- Random forest: about 80% accuracy on the test set
- Sex and passenger class showed the biggest differences in survival, which matches what I saw in the charts.

## What I'd do next
- Use cross-validation, since one train/test split can be lucky or unlucky.
- Tune the random forest's settings to see if it improves.

## How to run
Open `titanic_survival_prediction.ipynb` in Google Colab and run all cells.
The dataset loads automatically from seaborn.
