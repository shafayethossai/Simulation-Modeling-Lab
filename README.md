import numpy as np
from sympy import Matrix
import matplotlib.pyplot as plt
import seaborn as sns

// ****************************   DAY 1   *****************************

Task 1: 
# Sample scalar and array inputs
scaler = 3.7
arr = np.array([6, 5, 4, 3, 2, 1])

# Trigonometric functions
sin_values = np.sin(arr)
cos_values = np.cos(arr)
tan_values = np.tan(arr)
asin_values = np.arcsin(np.clip(arr / np.max(arr), -1, 1))  # Normalized and Clipping for valid range [-1, 1]
acos_values = np.arccos(np.clip(arr / np.max(arr), -1, 1))
atan_values = np.arctan(arr)

# Display results
print("sin:", sin_values)
print("cos:", cos_values)
print("tan:", tan_values)
print("asin:", asin_values)
print("acos:", acos_values)
print("atan:", atan_values)

Output:

sin: [-0.2794155  -0.95892427 -0.7568025   0.14112001  0.90929743  0.84147098]
cos: [ 0.96017029  0.28366219 -0.65364362 -0.9899925  -0.41614684  0.54030231]
tan: [-0.29100619 -3.38051501  1.15782128 -0.14254654 -2.18503986  1.55740772]
asin: [1.57079633 0.98511078 0.72972766 0.52359878 0.33983691 0.16744808]
acos: [0.         0.58568554 0.84106867 1.04719755 1.23095942 1.40334825]
atan: [1.40564765 1.37340077 1.32581766 1.24904577 1.10714872 0.78539816]



Task 2: 
# Creating a 3x2 matrix
matrix = np.array([[1.5, 2], [3.5, 4], [5.5, 6]])

# Trigonometric functions
sin_values = np.sin(matrix)
cos_values = np.cos(matrix)
tan_values = np.tan(matrix)
asin_values = np.arcsin(np.clip(matrix / np.max(matrix), -1, 1))  # Clipping for valid range [-1, 1]
acos_values = np.arccos(np.clip(matrix / np.max(matrix), -1, 1))
atan_values = np.arctan(matrix)

# Exponential and logarithm
exp_values = np.exp(matrix)
log_values = np.log(matrix)  # Natural logarithm (log base e)

# Absolute value and square root
abs_values = np.abs(matrix)
sqrt_values = np.sqrt(matrix)

# Remainder when divided by a scalar (e.g., 2)
rem_values = np.remainder(matrix, 2)

# Rounding functions
round_values = np.round(matrix)
floor_values = np.floor(matrix)
ceil_values = np.ceil(matrix)

# Display results
print("Matrix:\n", matrix)
print("\nsin:\n", sin_values)
print("\ncos:\n", cos_values)
print("\ntan:\n", tan_values)
print("\nasine:\n", asin_values)
print("\nacosine:\n", acos_values)
print("\natangent:\n", atan_values)
print("\nexp:\n", exp_values)
print("\nlog (natural):\n", log_values)
print("\nabs:\n", abs_values)
print("\nsqrt:\n", sqrt_values)
print("\nrem (remainder when divided by 2):\n", rem_values)
print("\nround:\n", round_values)
print("\nfloor:\n", floor_values)
print("\nceil:\n", ceil_values)

Output: 

Matrix:
 [[1.5 2. ]
 [3.5 4. ]
 [5.5 6. ]]

sin:
 [[ 0.99749499  0.90929743]
 [-0.35078323 -0.7568025 ]
 [-0.70554033 -0.2794155 ]]

cos:
 [[ 0.0707372  -0.41614684]
 [-0.93645669 -0.65364362]
 [ 0.70866977  0.96017029]]

tan:
 [[14.10141995 -2.18503986]
 [ 0.37458564  1.15782128]
 [-0.99558405 -0.29100619]]

asine:
 [[0.25268026 0.33983691]
 [0.62282659 0.72972766]
 [1.15965846 1.57079633]]

acosine:
 [[1.31811607 1.23095942]
 [0.94796974 0.84106867]
 [0.41113786 0.        ]]

atangent:
 [[0.98279372 1.10714872]
 [1.29249667 1.32581766]
 [1.39094283 1.40564765]]

exp:
 [[  4.48168907   7.3890561 ]
 [ 33.11545196  54.59815003]
 [244.69193226 403.42879349]]

log (natural):
 [[0.40546511 0.69314718]
 [1.25276297 1.38629436]
 [1.70474809 1.79175947]]

abs:
 [[1.5 2. ]
 [3.5 4. ]
 [5.5 6. ]]

sqrt:
 [[1.22474487 1.41421356]
 [1.87082869 2.        ]
 [2.34520788 2.44948974]]

rem (remainder when divided by 2):
 [[1.5 0. ]
 [1.5 0. ]
 [1.5 0. ]]

round:
 [[2. 2.]
 [4. 4.]
 [6. 6.]]

floor:
 [[1. 2.]
 [3. 4.]
 [5. 6.]]

ceil:
 [[2. 2.]
 [4. 4.]
 [6. 6.]]



Task 3:

# Creating a 2x3 matrix can have float values
vec = np.array([[1.5, 2, 3.1], [4, 5, 6.5]])

max_value = np.max(vec)
max_index = np.argmax(vec)  # Index of max element

# 2. Minimum value and index of min element
min_value = np.min(vec)
min_index = np.argmin(vec)  # Index of min element

# 3. Length of the vector
vec_length = len(vec)  # Equivalent to MATLAB's length()

# 4. Sorting in ascending order
sorted_vec = np.sort(vec)



# 5. Sum of elements
sum_values = np.sum(vec)

# 6. Product of elements
prod_values = np.prod(vec)

# 7. Median value
median_value = np.median(vec)

# 8. Mean value
mean_value = np.mean(vec)

# 9. Standard deviation
std_dev = np.std(vec)

# Display results
print("Max value:", max_value, "at index", max_index)
print("Min value:", min_value, "at index", min_index)
print("Length of vector:", vec_length)
print("Sorted vector:", sorted_vec)
print("Sum of elements:", sum_values)
print("Product of elements:", prod_values)
print("Median value:", median_value)
print("Mean value:", mean_value)
print("Standard deviation:", std_dev)

Output: 

Max value: 6.5 at index 5
Min value: 1.5 at index 0
Length of vector: 2
Sorted vector: [[1.5 2.  3.1]
 [4.  5.  6.5]]
Sum of elements: 22.1
Product of elements: 1209.0
Median value: 3.55
Mean value: 3.6833333333333336
Standard deviation: 1.717960677340692
