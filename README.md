### EX NO: 04
### DATE: 08.04.2022
# <p align="center"> BACK PROPOGATION IN SINGLE NEURON </P>

## AIM:
To write a python program to perform random classification.

## Equipments Required:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## Related Theoritical Concept:
    Backpropagation is an algorithm used to calculate derivatives quickly. It is a supervised learning algorithm, 
    for training Multi-layer Perceptrons. Artificial neural networks use backpropagation as a learning algorithm 
    to compute a gradient descent with respect to weights.  
    
## Algorithm:
### Step 1- 
   Inputs X, arrive through the preconnected path
### Step 2-
   Input is modeled using real weights W. The weights are usually randomly selected.
### Step 3- 
   Calculate the output for every neuron from the input layer, to the hidden layers, to the output layer.
### Step 4- 
   Calculate the error in the outputs
              ErrorB= Actual Output – Desired Output
### Step 5-
   Travel back from the output layer to the hidden layer to adjust the weights such that the error is decreased. Keep repeating the process until the desired output is achieved.
   
## Program:


```python

/*
Program to implement random classification.
Developed by   : P.Suganya
RegisterNumber :  212220230049
*/


#BACK PROPAGATION IN SINGLE NEURON
import numpy as np
i=1.5    #initial input
w_o=0.8  #initial weight
y=0.5    #desired response
r=0.01   #learning parameter
def dc_dw(a,y,i):
  dc_da=2*(a-y)
  da_dw=i
  return dc_da*da_dw
  
w=[w_o]
a=[w_o*i]
for j in range(0,100):
  a.append(w[-1]*i)
  w.append(w[-1]-r*dc_dw(a[-1],y,i))
  if(a[-1]-y)**2<0.001:
    break
print(a)
print(" ")
print(w)

```

## OUTPUT:

![EXP4_NN_O](https://user-images.githubusercontent.com/77089743/165778649-75d6dc4a-a368-4aed-9a9a-fded74d0b693.PNG)

## Result:
   Thus, the Bakpropagation for a single neuron was successfully implemented using python programming.
