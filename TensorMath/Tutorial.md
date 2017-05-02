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
*Example Matlab code* |  |
 | |
**Matrix times Vector** | |
*Expression* | ![Tensor](TensorMath6.svg) | ![Tensor](TensorMath7.svg)
*Example Matlab code*  | |
 | |
**Matrix times Matrix** | |
*Expression* | ![Tensor](TensorMath8.svg) | ![Tensor](TensorMath9.svg)
*Example Matlab code* | |
 | |
**Tensor times Vector** | |
*Expression* | NA | ![Tensor](TensorMath10.svg)
*Example Matlab code* | |
 | |
**Tensor Product** | |
*Expression* | NA | ![Tensor](TensorMath11.svg)
*Example Matlab code* | |

