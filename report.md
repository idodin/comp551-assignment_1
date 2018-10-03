# COMP 551 Fall 2018 - Assignment 1
## *Imad Dodin*
***

## Question 1 - Sampling

### 1. Pseudocode:
```
function sample():
  split interval (0, 1) into boundaries for each distinct outcome. # [[0,0.2], [0.2, 0.6], [0.6, 0.7], [0.7, 1.0]]
  generate a random float between 0 and 1.
  find which boundary set this is contained in
  return outcome associated to this boundary set
```

### 2. Sampling Results:
![Sampling Results](https://puu.sh/BE8us/a9c6d75203.png)

As is to be expected, a higher sample number makes our sampling method results tend closer to the provided probabilities. The percentage error between the fractions and provided probabilities are generally lower when sampling 1000 times, as shown by the Average Error printed in the output above.

***

## Question 2 - Model Selection

### 1. b. Data Visualization

![https://puu.sh/BEg1Y/421ccd1385.png](https://puu.sh/BEg1Y/421ccd1385.png)

![https://puu.sh/BEgiA/89f0a38aa4.png](https://puu.sh/BEgiA/89f0a38aa4.png)

### 1. c. Over or Underfitting

```
Training Data MSE:
6.4750601542578305
Validation Data MSE:
1415.7667845050064
```

This model is overfitting, as is made clear on the second plot whereby our predictions for the validation set drop rapidly and ignore the last green point (raw validation data). This causes a large value for the Mean Square Error of this model.

### 2. b. Regularization Comparisions

**Values for different lambda values**:

TODO

```
Training Data MSE:
9.20504017090436
Validation Data MSE:
9.699253211677858
Testing Data MSE:
128.56429805939945
```

### 2. c. Data Visualization

![https://puu.sh/BEgSi/99800b3e6c.png](https://puu.sh/BEgSi/99800b3e6c.png)

### 2. d. Over or underfitting

This model is underfitting as it does not adequately model the curves in the raw test data (in essence, the weights on the polynomial co-efficients should be larger.)

### 3. Degree of source polynomial.

By roughly tracing the raw test points from the previous example, one can hypothesize that the source polynomial is of roughly degree 10 or 11. It is difficult to be very precise about such a response due to the gaussian noise that has been added to the polynomial.

***

## Question 3: Stochastic Gradient Descents

### 1. b. MSE through Epochs

![https://puu.sh/BFg78/9d4fb96f3b.png](https://puu.sh/BFg78/9d4fb96f3b.png)

### 2. a. Validation Performance and Step Sizes
| Step Size | MSE on Validation Set |
|-----------|-----------------------|
| 1.00E+00  | 3.357589              |
| 1.00E-01  | 0.07414               |
| 1.00E-02  | 0.073831              |
| 1.00E-03  | 0.074067              |
| 1.00E-04  | 0.07407               |
| 1.00E-05  | 0.079338              |
| 1.00E-06  | 0.392337              |
| 1.00E-07  | 22.30903              |
| 1.00E-08  | 34.75164              |
| 1.00E-09  | 36.32894              |
| 1.00E-10  | 36.49057              |

### 2. b. Test Performance on Chosen Step Size (1.00E-02)

**Mean Squared Error (Test Set): 0.071703**

### 3. Epoch Visualizations:

**Epoch no. 500**:

![https://puu.sh/BFhhr/7900e493b5.png](https://puu.sh/BFhhr/7900e493b5.png)

**Epoch no. 1000**:

![https://puu.sh/BFhvo/24e4af2925.png](https://puu.sh/BFhvo/24e4af2925.png)

**Epoch no. 2500**:

![https://puu.sh/BFhwj/01e8923bf4.png](https://puu.sh/BFhwj/01e8923bf4.png)

**Epoch no. 4000**:

![https://puu.sh/BFhyE/2c85217caa.png](https://puu.sh/BFhyE/2c85217caa.png)

**Epoch no. 5000**:

![https://puu.sh/BFhAR/bd89c3d488.png](https://puu.sh/BFhAR/bd89c3d488.png)
