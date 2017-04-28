#### General expression

![Tensor](tensormath.svg)


Symbol | Meaning
---- | ------------------------
 D<sub>n</sub>  | dimensions, indexed by n 
 \|D<sub>n</sub>\| | size (cardinality) of dimension n

The expression above allows any dimension of the two arrays to be a singleton (ie range 1:1).  In such cases, the array(s) with the singleton dimension has its value *broadcast* to all elements along that dimension.  Then the array *T* can be constructed with consistent dimensions from the result of an element-wise operation.  *T* may subsequently be summed along a given dimension (a reduction).
