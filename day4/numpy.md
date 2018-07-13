## Numpy

Features

* N dimentional arrays
* broadcasting (element by element operations)
* core linear algebra operations
* communicate with Fortran/C++/C

Differences with python inbuilt datatypes

* better than lists and dictionaries
* python list you can store any data type but in ndarrays you are restricted to a datatype, which means you can be store set of integers or floats etc.
* better performance

### Attributes of an np array

* shape - returns a tuple for example a matrix with n rows and m cols returns (n,m) tuple
* size - total # of items in an array, which is the product of elements in shape ex 5X5 array has 25 items
* ndim - # of axis which is len(shape)
* dtype - represents the type of the elements of an array. Can be derived from python default types but also has numpy sophesticated types.
* data - databuffer for the acutal data
* itemsize - # of bytes of each element in the array

```python
import numpy as np

ndarr = np.empty((5,5),dtype=np.int16)

print(ndarr.shape)
print(ndarr.dtype)
print(ndarr.ndim)
print(ndarr.size)
print(ndarr.itemsize)
print(ndarr.data)

# result
(5, 5)
int16
2
25
2
<memory at 0x7f80dc137a68>
```

### Various ways of creating an np array

* array - create an array from python list
* zeros - numpy creates an array with all 0s'
* ones - creates an array with all ones
* empty - creates an array with random data
* arange - create an array from a given range
* linspace - create an array with linearspace between two elements
* logspace - creates an array between two elements in a log space

```python
import numpy as np

alist = [1,2,3]
arr = np.array(alist) # prints an array with one row,3 cols

arr.ones(5) # creates an array of 5 ones
arr.ones(5 ,5) # throws an error
arr.ones([5,5]) # creates an array of ones with 5 rows and 5 columns

arr.zeros(5) # creates an array of 5 zeros

arr.arange(100) # creates an array from 0..99
arr.linspace(0,1, 100) # linearly space between 0 to 1 by 100
arr.logspace(0,1,100, base=10.0) # log space between 0 to 1
```