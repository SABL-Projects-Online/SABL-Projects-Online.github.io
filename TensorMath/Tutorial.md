###### *GPU Posterior Simulation - Bayesian Simulated Annealing - Quantum Annealing*
# SABL-Projects: Common matrix operations in tensor form
[Return to Main Page](/)
#### General expression

![Tensor](tensormath.svg)


Symbol | Meaning
---- | ------------------------
 D<sub>n</sub>  | dimensions, indexed by n 
 \|D<sub>n</sub>\| | size (cardinality) of dimension n

Explanation:
The expression above allows any dimension of the two arrays to be a singleton (ie range 1:1).  In such cases, the array(s) with the singleton dimension has its value *broadcast* to all elements along that dimension.  Then the array *T* can be constructed with consistent dimensions from the result of an element-wise operation.  *T* may subsequently be summed along a given dimension (a reduction).

For brevity, 5 dimensions are explicitly described, even though the number of dimensions can be arbitrarily large (higher dimensions that have not been explicitly described are assumed to be 1:1 ie singletons).
 
*Form*    | Common | High dimensional
--------- | ------ | ----------------
**Scalar time Matrix** | |
*Expression* | ![Tensor](TensorMath2.svg) | ![Tensor](TensorMath3.svg)
*Example Matlab code* | ```beta = 0.6; X = rand(8,10); T = beta*X;``` | ```beta = 0.6; X = rand(1,1,8,1,10); T = beta*X;```
 | |
**Vector times Vector Outer Product** |  | 
*Expression* | ![Tensor](TensorMath4.svg) | ![Tensor](TensorMath5.svg)
*Example Matlab code* | ```beta = rand(18,1); X = rand(1,14); T = beta*X;```  | ```beta = rand(1,1,1,18,1); X = rand(1,14,1,1,1); T = bsxfun(@times,beta,X);```
 | |
**Matrix times Vector** | |
*Expression* | ![Tensor](TensorMath6.svg) | ![Tensor](TensorMath7.svg)
*Example Matlab code*  | ```beta = rand(14,16); X = rand(16,1); T = beta*X;``` | ```beta = rand(1,1,1,16,1); X = rand(1,1,1,16,14); T = bsxfun(@times,beta,X); T = sum(T,4);```
 | |
**Matrix times Matrix** | |
*Expression* | ![Tensor](TensorMath8.svg) | ![Tensor](TensorMath9.svg)
*Example Matlab code* | ```beta = rand(12,16); X = rand(16,14); T = beta*X;``` | ```beta = rand(1,1,12,16,1); X = rand(1,1,1,16,14); T = bsxfun(@times,beta,X); T = sum(T,4);```
 | |
**Tensor times Vector** | |
*Expression* | NA | ![Tensor](TensorMath10.svg)
*Example Matlab code* | | ```beta = rand(18,14,12,10,1); X = rand(1,14,1,10,1); T = bsxfun(@times,beta,X); T = sum(sum(T,4),2);```
 | |
**Tensor Product** | |
*Expression* | NA | ![Tensor](TensorMath11.svg)
*Example Matlab code* | | ```beta = rand(12,1,14,1,1); X = rand(1,18,1,1,20); T = bsxfun(@times,beta,X);```

[Return to Main Page](/)
