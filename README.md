# AbelardoRadny_2ECE-A_PA2

NORMALIZATION

``` python
import numpy as np #Importing numpy to the code
X = np.random.random((5,5)) #creating a random 5x5 array and storing it to variable X
M = X.mean() #getting the mean from variable X and storing it to variable M
STD = X.std() #getting the standard deviation from variable X and storing it in variable STD
Z = (X-M)/STD #solving the nomralization using the formula and saving it to variable Z
```

