# COMP 551 Fall 2018 - Assignment 1
## *Imad Dodin*
***

## Question 1 - Sampling

**1. Pseudocode**:
```
function sample():
  split interval (0, 1) into boundaries for each distinct outcome. # [[0,0.2], [0.2, 0.6], [0.6, 0.7], [0.7, 1.0]]
  generate a random float between 0 and 1.
  find which boundary set this is contained in
  return outcome associated to this boundary set
```

**2. Sampling Results:**
![Sampling Results](https://puu.sh/BE8us/a9c6d75203.png)

As is to be expected, a higher sample number makes our sampling method results tend closer to the provided probabilities. The percentage error between the fractions and provided probabilities are generally lower when sampling 1000 times, as shown by the Average Error printed in the output above.

## Question 2 - Model Selection

**1. b. Data Visualization**

![https://puu.sh/BEg1Y/421ccd1385.png](https://puu.sh/BEg1Y/421ccd1385.png)

![https://puu.sh/BEgiA/89f0a38aa4.png](https://puu.sh/BEgiA/89f0a38aa4.png)

**1. c. Over or Underfitting**

```
Training Data MSE:
6.4750601542578305
Validation Data MSE:
1415.7667845050064
```

This model is underfitting, as is made clear on the second plot whereby our predictions for the validation set drop rapidly and ignore the last green point (raw validation data). This causes a large value for the Mean Square Error of this model.
