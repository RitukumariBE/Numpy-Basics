# **_Numpy-Basics_**

## _Table of content_ :-
            1. Introduction
            2. Installation
            3. Creation of Numpy arrays
            4. Properties and Attributes of Numpy arrays
            5. Numpy Arrays v/s Python Lists
            6. Indexing,Slicing and Iteration
               1. Fancy Indexing
               2. Indexing with Boolean Arrays
            7.  Operations in Numpy Arrays
            8.  Reshaping of Numpy Arrays
            9.  Ploting Graphs Using Numpy
            10. Broadcasting

## _Introduction to Numpy_:-
   _Numpy is a low level library of python written in C and FORTAN for high level mathematical function. It provides support for creating and managing large, multidimensional arrays and matrices, along with a collection of mathematical functions to operate on them efficiently._

## Installation
    1.Open your terminal in your VScode or any other text editor.
    2.Write and run 'pip install numpy'.
    3.Installation Done 


## Creation of Numpy Arrays
   #### 1. **`np.array()`** : It is a function used to create the array for any dimension.
        eg:- 1.for 1-D array
               array1 = np.array([1,2])
               Output :- array([1, 2])
             2.for 2-D array
               array2 = np.array([[1,2,3],[4,5,6]])
               Output :- array([[1, 2, 3],
                                [4, 5, 6]])
            and so on

   #### 2. **`np.zeros()`** : It is a function used to create a array with any given shape in tuple form whose each element initialize with zero
        eg:- np.zeros((2,2))
            Output:-array([[0., 0.],
                           [0., 0.]])

   #### 3. **`np.ones()`** : It is a function used to create a array with any given shape and initialize each element of array with one. 
        eg:- np.ones((2,2))
            Output:-array([[1., 1.],
                          [1., 1.]])

   #### 4. **`np.arange()`** : It is a function to create a array within a range 
        eg:- np.arange(1,20,2) ,1-lower limit,2-upper limit,2-steps between two numbers
             Output:-array([ 1,  3,  5,  7,  9, 11, 13, 15, 17, 19])

   #### 5. **`np.linspace()`**: It is a function to create a array within a range where each element of array is equidistant to other element 
        eg:- np.linspace(1,20,5) ,Creates a 1-D array with 5 equidistant values between 1 and 20.
             Output:-array([ 1.  ,  5.75, 10.5 , 15.25, 20.  ])

   #### 6. **`np.copy()`** : It is a function to copy to already existing array

   #### 7. **`np.identity()`** : It is a function used to create a identity array(diagonal elements are 1 and rest are 0) 
        eg:- np.identity(3) ,3-size of the matrix
             Output:-array([[1., 0., 0.],
                            [0., 1., 0.],
                            [0., 0., 1.]])

## Properties and Attributes of Numpy Arrays
 - Shape:-The shape of a NumPy array describes elements the array has in each dimension.
      * For 1D arrays, the shape is a single number (the length of the array).
      * For 2D arrays, the shape is a tuple with two values (rows, columns),and so on for higher-dimensional  arrays.
  
 - ndim:- The ndim of a NumPy array describes the dimension of the array.
      * array = np.array([[1,2],[3,4]])  
        array.ndim  
        Output:- 2

 - Size:- The Size of a NumPy array describe the number of elements in a array which is multiplication of all elements of shape.
      * array.size  
        Output:- 4

 - Itemsize:- The itemsize of a NumPy array describe the size that the each element take in the array.
      * array.itemsize  
        Output:- 8

 - Dtype:- The Dtype of a NumPy array describe the type of date which is stored in the array.
      * array.Dtype  
        Output:-int64

 - astype():- The astype of a NumPy is used to convert the datatype of elements of array.
      * array.astype('float32')

## Why we choose NumPy Arrays over Python Lists ?
  1. Arrays Operation take less time in compare to list operations.
  2. Arrays are convenient in use.
  3. Arrays take less memory compare to List.
   
## Indexing,Slicing and Iteration 
 - Indexing :- Indexing in NumPy arrays allows you to access specific elements or a range of elements in an array.
           * For 1D arrays, you can access elements using a single index (starting from 0).
               Example:- arr_1d = np.array([10, 20, 30, 40])  
                         print(arr_1d[2])  
                         Output: 30 
           * For 2D arrays, you use two indices: one for the row and one for the column. 
               Example:- arr_2d = np.array([[1, 2], [3, 4], [5, 6]])
                         print(arr_2d[1, 0])  
                         Output: 3  (Access element at row 1, column 0)

     ### Forms of Indexing:-
        1. Fancy Indexing :- This type of indexing allows you to access multiple elements in a non-sequential order             
                    Example:- arr = np.array([10, 20, 30, 40, 50])
                              result = arr[0, 2, 4]  ,0,2,4 are indices where we want to indice
                              print(result)  
                              Output: [10 30 50]
 
        2. Indexing with Boolean Arrays :- Boolean indexing involves using boolean values (True or False) to filter elements of an array.
                    Example:- arr = np.array([1, 2, 3, 6, 7, 8])
                              bool_array = arr > 5
                              print(bool_array)   
                              Output: [False False False  True  True  True]

 - Slicing:- Slicing in NumPy refers to the process of selecting a subset of elements from an array.    
    * syntax - **`array[start:stop:step]`**  
            
          Example:- arr = np.array([10, 20, 30, 40, 50])
                    sliced_arr = arr[1:4]
                    print(sliced_arr)
                    Output:-[20 30 40]

 - Iteration:- Iteration in NumPy allows you to loop through the elements of an array to perform operations.  
             
          Example:- arr = np.array([10, 20, 30, 40, 50])  
                    for element in arr:  
                    print(element)   
                    Output:-  10  
                              20  
                              30  
                              40  
                              50  
               

## Operations in NumPy Array
### 1.Basic Operations
Basic operations in NumPy are performed element-wise. They include arithmetic, relational, and logical operations.

#### 1.Arithmetic Operations:-
          Perform mathematical operations between arrays or between arrays and scalars:

               Addition: array1 + array2
               Subtraction: array1 - array2
               Multiplication: array1 * array2
               Division: array1 / array2

#### 2.Relational Operations:-
          Compare elements of arrays using relational operators:

               Greater than (>)
               Less than (<)
               Equal to (==)
               Greater than or equal to (>=)
               Less than or equal to (<=)

#### 3.Logical Operations
          Combine conditions across arrays:

               Logical AND: &
               Logical OR: |
               Logical NOT: ~

### 2. Unary Operations
          Unary operations act on individual elements of a NumPy array.

#### Common Unary Operations
          Absolute Value: np.abs(array) → Returns the absolute value of all elements.
          Negative: -array → Negates all elements in the array.
          Square Root: np.sqrt(array) → Computes the square root of all elements (non-negative).

### 3. Universal Functions (ufuncs)
          Universal functions (ufuncs) are NumPy's optimized functions for element-wise operations.

               Mathematical Functions
               Perform advanced mathematical computations:

               Trigonometric Functions: np.sin(array), np.cos(array), np.tan(array)
               Exponential Function: np.exp(array)
               Logarithmic Functions: np.log(array), np.log10(array), np.log2(array)

### 4. Statistical Operations
          Summarize data from arrays:

               Sum: np.sum(array)
               Mean: np.mean(array)
               Standard Deviation: np.std(array)

### 5. Reduction Operations
          Aggregate array values into single values:

               Minimum: np.min(array)
               Maximum: np.max(array)
               

## Reshaping of NumPy arrays
          Reshaping in NumPy allows you to modify the structure of an array without changing its data.

####  Methods of reshaping :-

   |                  |                                                        |
   |------------------|--------------------------------------------------------|
   |1. Reshaping:-    | Changes the shape of an array to the specified dimensions.|
   |                  | Syntax: array.reshape(new_shape)                         |
   |2. Ravel:-        | Converts an array into a flattened 1D array. Unlike flatten(), it returns a view  |
   |                  |(modifying it affects the original array).|
   |                  |Syntax: np.ravel(array)|
   |3. Transpose:-    |Flips the dimensions of an array (e.g., rows become columns).|
   |                  |Syntax: array.T or np.transpose(array)|
   |4. Stacking:-     |Stacking combines multiple arrays into one along different axes.|
   |                  |Syntax: np.hstack((array1, array2))|
   |                  |        np.vstack((array1, array2))|
   |5. Splitting:-    |Splitting breaks arrays into smaller sub-arrays.|
   |                  |Syntax: np.hsplit(array, n)|
   |                  |        np.vsplit(array, n)|

## Ploting Graph using NumPy
          a. Import NumPy for data and Matplotlib for plotting.

          b. Create Data
             Use NumPy functions like arange, linspace, or mathematical functions to generate data points.

          c. Plot the Data
             Use Matplotlib’s plot() function to create a graph.

          d. Customize the Plot
             Add labels, titles, legends, and styles for better visualization.

          e. Display the Plot
             Use plt.show() to display the graph.

## Broadcasting  
     The term broadcasting refers to the ability of NumPy to treat arrays of different shapes during arithmetic operations.

#### Rules for Broadcasting:-
  * if x = m and y = n , operation will take place.  
     Example:- a1 = np.arange(8).reshape(2,4)  
               a2 = np.arange(8,16).reshape(2,4)  
               a1+a2    

  * if x = 1 and y = n then also operation will take place(same dimension).  
     Example:- a1 = np.arange(3).reshape(1,3)  
               a2 = np.arange(12).reshape(4,3)  
               a1 + a2  
  
  * if y = 1 and x = m then also operation will take place ,even if they are not of the same dimension.  
     Example:- a1 = np.arange(4).reshape(4,1)  
               a2 = np.arange(12).reshape(4,3)  
               a1 + a2  

  * if x = 1 and y !=n then also operation will not take place.  
     Example:- a1 = np.arange(3).reshape(1,3)  
               a2 = np.arange(16).reshape(4,4)  
               a1 + a2  

  * if x = 1 and n = 1 then y == m ,operation will take place.  
     Example:- a1 = np.arange(3).reshape(1,1)  
               a2 = np.arange(3).reshape(3,1)  
               a1 + a2  

  * if x = 1 and y = 1 , then the operation will take place.  
     Example:- a1 = np.arange(1).reshape(1,1)  
               a2 = np.arange(20).reshape(4,5)  
               a1 + a2


## Some Functions Of NumPy
##  NumPy Random Module

### 1️⃣ randint()
Generates random integers within a specified range.

**Purpose:**  
Used when we need whole numbers such as marks, counts, IDs, etc.

**Example Use Case:**  
Generating student marks between 0 and 100.

---

### 2️⃣ rand()
Generates random floating-point numbers between 0 and 1.

**Purpose:**  
Useful for probability simulations and normalized data.

---

### 3️⃣ randn()
Generates random numbers from a standard normal distribution  
(mean = 0, standard deviation = 1).

**Purpose:**  
Commonly used in statistics and machine learning.

---

### 4️⃣ random()
Generates random floating-point numbers between 0 and 1.

Similar to `rand()` but used differently in shape specification.

---

### 5️⃣ choice()
Selects random elements from a given array.

**Purpose:**  
Useful for sampling data or randomly selecting categories.

---

### 6️⃣ seed()
Sets a fixed starting point for random number generation.

**Why it matters:**  
- Ensures reproducibility
- Same random numbers are generated every time

Very important in machine learning experiments.

---

## 📊 Shapes in Random Functions
Most NumPy random functions allow specifying:

- Number of rows
- Number of columns
- Multi-dimensional shapes

This makes it easy to create structured datasets such as:
- Student mark tables
- Image pixel data
- Simulation matrices

---

## 🛠 Concepts Practiced
- Generating 1D arrays
- Generating 2D arrays
- Understanding shapes
- Random sampling
- Reproducibility using seed

---

## 🚀 Practical Applications
- Creating dummy datasets for analysis
- Monte Carlo simulations
- Weight initialization in neural networks
- Random sampling for experiments
- Statistical modeling

---

## 👤 Author
Ritu Kumari  
Learning NumPy fundamentals with practical implementation.

