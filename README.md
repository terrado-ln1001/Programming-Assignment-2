# Programming-Assignment-2
A repository that contains 2 problems using numpy. **Normalization Problem** is asking to take a data (the ndarray X) and apply the said formula. **Divisible by three** is asking to select all the elements from the array whose values can be evenly divided by 3 with no remainder.

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
---------------------------------
## Divisible by Three
This problem helps practice working with arrays in NumPy. It shows how to generate squared numbers, reshape them into a 10×10 array, and select elements that are divisible by 3, which practices conditional filtering in arrays.

### Step-by-Step
#### 1. Create number from 1 to 100
Use np.arange(1, 101) to generate the first 100 positive integers. The range uses (1,101) instead of just (1,100) is because the end value in np.arange is exclusive, so writing 101 ensures that 100 is included in the sequence.
```python
x = np.arange(1, 101)
```
#### 2. Square Each Number
The problem asks to square the first 100 positive integers. Each number in the array is squared using the operator ** 2, where ** in Python is used for exponentiation. This means every element is multiplied by itself.
```python
squares = x ** 2
```
#### 3. Reshape into 10x10 array
After squaring the numbers, the array is reshaped into a 10×10 format using .reshape(10, 10). This organizes the squared values neatly into a 2D array with 10 rows and 10 columns.
```python
A = squares.reshape(10, 10)
```
#### 4. Select Elements Divisible by 3
Next is applying a condition to check which numbers are divisible by 3 using A % 3 == 0. The % operator gives the remainder of division, so numbers with remainder 0 are divisible by 3.
```python
div = A[A % 3 == 0]
```
