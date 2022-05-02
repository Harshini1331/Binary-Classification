### EX NO: 02
### DATE:
# <p align="center">BINARY CLASSIFICATION</p> 
## Aim:
To write a python program to perform binary classification.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner /Google Colab

## Related theoretical concepts:
Binary classification refers to predicting one of two classes and multi-class classification involves predicting one of more than two classes. Binary classification is the task of classifying the elements of a set into two groups on the basis of a classification rule.

## Algorithm
1.Define dataset.<br>
2.Summarize dataset shape.<br>
3.Summarize observations by class label.<br>
4.Summarize first few examples.<br>
5.Plot the dataset and color the by class label.


## Program:
Program to implement binary classification.<br>
Developed by: Harshini M<br>
RegisterNumber: 212220230022

```python
from numpy import where
from collections import Counter
from sklearn.datasets import make_blobs
from matplotlib import pyplot

X,y = make_blobs(n_samples=10,centers=2,random_state=1)
print(X.shape,y.shape)
counter=Counter(y)
print(counter)

for i in range(5):
    print(X[i],y[i])
    
for label, _ in counter.items():
    row_ix=where(y==label)[0]
    pyplot.scatter(X[row_ix,0], X[row_ix,1], label=str(label))
pyplot.legend()
pyplot.show()

```

## Output:
![screenshot1](https://user-images.githubusercontent.com/75235554/163706496-0a5e4b92-9e2c-444d-ae74-81a4543a118c.jpg)

## Result:
Thus the python program performed binary classification successfully.
