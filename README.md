# AbelardoRadny_2ECE-A_PA2

NORMALIZATION

``` python
import numpy as np #Importing numpy to the code
X = np.random.random((5,5)) #creating a random 5x5 array and storing it to variable X
M = X.mean() #getting the mean from variable X and storing it to variable M
STD = X.std() #getting the standard deviation from variable X and storing it to variable STD
Z = (X-M)/STD #solving the normalization using the formula and saving it to the variable Z
np.save("X_normalized.nyp", Z) #saving the normalization code into a numpy file
print("Normal Array:\n", X)
print("Normalized Array:\n", Z) #printing both the random normal array and the normalized array
```

Divisible by 3

``` python
A=np.arange(1,101) #getting an array with the elements of 1-100 and storing it in the variable A
np.shape(A) #loading the shape of the array A
square=A.reshape(10,10)**2 #reshaping array A into a 10x10 array and squaring each and every element inside the array, storing it to variable square
divisible_by_3 = square[square%3 == 0] #taking all of the variables ofthe  array square and looking for every element divisible by 3 using modulo, storing it to the variable divisible_by_3
np.save("div_by_3.npy", divisible_by_3) #saving the code of divisible_by_3 into a numpy file
print("10x10 array: \n", square)
print("Numbers divisible by 3:\n", divisible_by_3) #printing both the squared 10x10 array and the array with the elements divisible by 3
```
