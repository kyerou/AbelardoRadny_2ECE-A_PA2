# ECE2112 PA2

Numpy

This problem assignment made us use numpy to complete certain tasks for this assignment.

# NORMALIZATION
This problem made us create a 5x5 ndarray and find its normalization using the code for mean '.mean()', and standard deviation '.std()'

First, we import numpy
``` python
import numpy as np #Importing numpy to the code
```
Now create a 5x5 ndarray with random numbers:
```python
X = np.random.random((5,5)) #creating a random 5x5 array and storing it to variable X
```
random.random sends out random values into the ndarray

To compute the mean, I used .mean():
```python
M = X.mean() #getting the mean from variable X and storing it in variable M
```

To compute the standard deviation, I used .std():
```python
STD = X.std() #getting the standard deviation from variable X and storing it to variable STD
```

Now, since I have all of the things I need to compute for the normalization, I  used the formula: 

<img width="117" height="69" alt="Image" src="https://github.com/user-attachments/assets/83817f04-97ea-439c-9db9-ca2521fd5d2d" />

Translating it to python, which was:
```python
Z = (X-M)/STD #solving the normalization using the formula and saving it to the variable Z
```
Now, to save a certain variable into a numpy file, I used np.save():
```python
np.save("X_normalized.nyp", Z) #saving the normalization code into a numpy file
```

Lastly, to check if it was correct, I printed the original ndarray and now the normalized ndarray using print():
```python
print("Normal Array:\n", X)
print("Normalized Array:\n", Z) #printing both the random normal array and the normalized array
```

# Divisible by 3
The task for this was to make a 10x10 ndarray that is square, then determine the values that are divisible by 3.

First was to make an array that contains numbers from 1-100
``` python
A=np.arange(1,101) #getting an array with the elements of 1-100 and storing it in the variable A
```

Next was to reshape the array into a 10x10 using .reshape()
```python
np.shape(A) #loading the shape of the array A (this is necessary to do first before reshaping it)
square=A.reshape(10,10)**2 #reshaping array A into a 10x10 array and squaring each and every element inside the array, storing it to variable square
```
In the same line of code, I already squared the results inside the 10x10 array using the arithmetic **2

Now to get the divisible by 3, I used the modulo (%) arithmetic, then equating the results to zero to showcase the values that have 0 as a result of modulo 3:
```python
divisible_by_3 = square[square%3 == 0] #taking all of the variables of the  array square and looking for every element divisible by 3 using modulo, storing it to the variable divisible_by_3
```

Saving the divisible by 3 variable into a numby file:
```python
np.save("div_by_3.npy", divisible_by_3) #saving the code of divisible_by_3 into a numpy file
```

To check if it was all correct, I used print() to see the results:
```python
print("10x10 array: \n", square)
print("Numbers divisible by 3:\n", divisible_by_3) #printing both the squared 10x10 array and the array with the elements divisible by 3
```
