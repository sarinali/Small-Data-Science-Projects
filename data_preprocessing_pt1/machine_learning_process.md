# Machine Learning Process

- Data Pre-processing: includes importing the data, cleaning it and splitting it into training and test
- Model: build the model, train it, make prediction
- Evaluation: calclate performance, making verdicts

## Training Set and Test Set

80% is training set
- used to build the model

20% is testing set
- not used in the testing set 

## Feature Scaling

| Person      | Income | Age |
| ----------- | ----------- | ----------- |
| 1      | 70k       |45       |
| 2   | 60k        |44        |
| 3   | 45k        |40        |

Which person is person 2 more similar to (1 or 2)

Normalization:

$$X' = \frac{X-X_{min}}{X_{max}-X_{min}}$$

Values fall betweeen $[0,1]$, apply normalization to the columns above 

Standardization ($\mu$ = standard deviation of $x$):

$$X_{s} = \frac{X-mean(x)}{\mu}$$

Values fall between $[-3,3]$, they can go above or below depending on how much of an outlier the data is 

**Normalization** works for when your data has a binomial distribution but **standardization** works for any dataset

| Person      | Income | Age |
| ----------- | ----------- | ----------- |
| 1      | 1       |1       |
| 2   | 0.444..       |0.8        |
| 3   | 0        |0        |

Person 2 is closer to Person 3 income wise but closer to person 1 age wise. (0.44.. to 0 and 0.8 to 1)

