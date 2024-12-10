# Project: Randomized Numerical Linear Algebra (rNLA)

Course: DSC 210: Numerical Linear Algebra

Instructor: Dr. Tsui-wei Weng

Authors: Sunil Madhow, Samyak Karnavat, Erchi Wang, Brandon Hsu

## Experiments

The purpose of the experiments is to compare the accuracy and runtime of methods performed with/without rNLA.

- [Approximate Matrix Multiplication](amm.ipynb)
- [Randomized Singular Value Decomposition](rsvd.ipynb)
- [Image Compression](imgCompress.ipynb)

> [!NOTE]
> Libraries in [requirements.txt](requirements.txt) must be installed before running the experiments/notebooks


## Results

### Matrix Multiplication

These experiments implement two versions of randomized matrix multiplication. One uses subsampling with uniform weights, and one uses subsampling with optimal weights. We compare the runtime of randomized matrix multiplication with that of numpy's built in matrix multiplication functionality. We also compare the error of each approximation scheme with respect to the output of numpy's built in matrix multiplication function. The results below can be obtained by running the jupyter notebook ``matrix_mul.ipynb`` , provided that the requirements in ``requirements.txt`` are configured. The whole notebook should take roughly n minutes to run.

#### Runtime
![Mat mul runtimes](https://github.com/bhdsc/rNLA/blob/main/visualizations/exp1_times.png)

### Errors
![Mat mul errors](https://github.com/bhdsc/rNLA/blob/main/visualizations/exp1_errors.png)



| Singular Value Decomposition | Randomized Singular Value Decomposition |
|------------------------------|-----------------------------------------|
| error vs. dimension plot     | error vs. dimension plot                |
| runtime vs. dimension plot   | runtime vs. dimension plot              |

## References

For a full list of references, see our [report](README.md).


### Image Compression
