### PROGRAMMING-ASSIGNMENT 2

#### NORMALIZATION PROBLEM - WE ARE TASKED TO CREATE A 5X5 ARRAY AND MAKE THE VALUES NORMALIZED

1. First, I imported numpy as np to make the coding possible and not lead to error
 ```python
import numpy as np
```

2. I then went on to make the randomized array
```python
X = np.random.rand(5, 5)
print("Original array: ")
print(X) #create a randomized array
```

3.  I then find the mean of the array as it will be used later
```python
ean_val = np.mean(X) #to calculate the mean of the values in the array
```

4. similarly, I would find the standard deviation as it will be used later on
```python
std_val = np.std(X) #to calculate the standard deviation of the values in the array
```

5. I then used the found values for the mean and the standard deviation to obtain the normalized values in the array
```python
X_normalized = (X - mean_val) / std_val #calculate the earlier values to normal
```

6. I saved the np
```python
np.save('X_normalized.npy', X_normalized)
```

7. I then printed the values
```python
 print("Normalized array:")
print(X_normalized)
```


#### DIVISIBLE BY 3 PROBLEM - WE ARE TASKED TO CREATE A 10 X 10 ARRAY AND HAS ALL VALUES DETERMINED TO BE DIVISIBLE BY 3


1. I imported numpy to make this possible
```python
import numpy as np
```

2. I then made an array of 1-100 to place the values
```python
numbers = np.arange(1, 101) #makes an array of 1-100 
numbers
```

3. I then added the squares of the numbers in the array
```python
squares = numbers ** 2 #to square the values in the array
```

4. I reformatted the new array into a 10 x 10 matrix array
```python
A = squares.reshape(10, 10) #reshape the current array into a 10x10 matrix format
```

5. I used a boolean to determine which values in the array were divisible by 3
```python
div_by_3 = A[A % 3 == 0] #determine the values divisible by 3 using boolean indexing
```

6. I saved the np
```python
np.save('div_by_3.npy', div_by_3)
```

7. I printed the values
```python
print("\nElements divisible by 3:")
print(div_by_3)
```
