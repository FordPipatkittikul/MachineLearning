# Numpy

It is an open source library which helps you do numerical computing.

# Why NumPy?

You can do numerical calculations using pure Python. but the main reasons you use NumPy is because it's fast. Behind the scenes, the code has been optimized to run using C. Which can do things much faster than Python.

There is a process called vectorization. Vectorization(a linear transformation which converts a matrix into a column vector) aims to do calculations by avoiding loops as loops can create potential bottlenecks.

    
    import numpy as np

    a = np.array([1, 2, 3])
    b = np.array([10, 20, 30])
    result = []
    
    # Example (non-vectorized):

    for i in range(len(a)):
        result.append(a[i] + b[i])

    # Example Vectorized version:

    result = a + b

NumPy achieves vectorization through a process called broadcasting(NumPy's smart way of making arrays with different shapes work together during operations.).