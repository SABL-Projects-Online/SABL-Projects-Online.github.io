#### General expression

![Tensor](tensormath.svg)


Symbol | Meaning
---- | ------------------------
 D<sub>n</sub>  | dimensions, indexed by n 
 \|D<sub>n</sub>\| | size (cardinality) of dimension n

Explanation:
The expression above allows any dimension of the two arrays to be a singleton (ie range 1:1).  In such cases, the array(s) with the singleton dimension has its value *broadcast* to all elements along that dimension.  Then the array *T* can be constructed with consistent dimensions from the result of an element-wise operation.  *T* may subsequently be summed along a given dimension (a reduction).

For brevity, 5 dimensions are explicitly described, even though the number of dimensions can be arbitrarily large (higher dimensions that have not been explicitly described are assumed to be 1:1 ie singletons).

#### Scalar times Matrix 

Common form | High dimensional form
----------- | ---------------------
![Tensor](TensorMath2.svg) | ![Tensor](TensorMath3.svg)
Matlab code | Matlab code
```beta = 0.6; X = rand(8,10); T = beta*X;``` | ```beta = 0.6; X = rand(1,1,8,1,10); T = beta*X;```

#### Vector times Vector Outer Product

#### Matrix times Vector

#### Matrix times Matrix

#### Matrix Matrix Kron Product

#### Tensor times Vector

#### Tensor Product
