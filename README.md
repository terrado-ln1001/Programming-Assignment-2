# Programming-Assignment-2
A repository that contains 2 problems using numpy. Normalization Problem is asking to take a data (the ndarray X) and apply the said formula. Divisible by three is asking to select all the elements from the array whose values can be evenly divided by 3 with no remainder.

## Learning Outcomes
1. To identify the codes and functions incorporated in the Numpy library
2. To be able to apply and use the different codes and functions in creating a Python program using a Numpy library
-----------------------------------------------------------
## Normalization Problem
This problem helps practice data preprocessing with NumPy. It shows how to normalize data by subtracting the mean and dividing by the standard deviation, which makes the data easier to analyze.

### Step-by-Step
#### 1. Create the data
The first step is to create the data. A data that is a random 5 x 5 ndarray and store it to variable x.
```python
x = np.random.rand(5, 5)
```
#### 2. Normalize the data
This is then followed by normalizing the data X using the normalization formula. The mean is obtained with the element-wise .mean() function, and the standard deviation is obtained with the element-wise .std() function.
```python
x_normalized = (x - x.mean()) / x.std()
```
#### 3. Save the data as .npy
After normalization, the data is saved into a file using the NumPy function np.save(). This stores the array in a file with the .npy extension. This allows the processed array to be stored and reloaded later when needed.
```python
np.save ("x_normalize.npy", x_normalized)
```

