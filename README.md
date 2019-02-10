# Titanic
Project to determine if a person survived Titanic disaster.

## Dataset
Dataset for this project can be found by this link --> https://www.kaggle.com/c/titanic/data

## Pre-processing
### Age
* Assigned the missing age values with mean female age or mean male age accordingly.

### Fare
* Not many fare values are missing.
* So, replaced all the missing fares with 0.

### Embarked
* Based on the fare the missing Embarked was replaced.
* Replaced missing Embarked value with E if the fare was above 50.
* Replaced missing Embarked value with C if the fare was above 25 and below 50.
* Replaced missing Embarked value with Q if the fare was below 25.

### Cabin
* Since cabin values have a lot of missing values, it can be ignored.

### Passenger-Id
* Passenger Id is a unique value for each person. So, this will not help to determine the survival and hence is dropped.

### Sex
* Encoded the attribute of Sex.

### Embarked
* Encoded the value of Embarked.

### Name titles
* Name by itself is not an important feature.
* So, it's split to get the title of the name.
* It is then encoded based on the probability of their survival. The one with highest probability is given higher value.

### Tickets
* Generating feature from Ticket.
* The first letter of the ticket is used if letter is present else NA. 
* Encoded the letters.

### Family count
* Generated feature for family count using parch and sibsp.

## Scaling
* Scaled the date using StandardScalar.

## Cross Validation
* Performed cross validation using the train data to find the best 'c' and 'gamma' value for SVM.

## Model
* Used SVM with the best parameters achieved in Cross Validation.

## Score
* This approach gave a score of 80.3% accuracy.
