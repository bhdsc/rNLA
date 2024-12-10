# Project: Randomized Numerical Linear Algebra (rNLA)

Course: DSC 210: Numerical Linear Algebra

Instructor: Dr. Tsui-wei Weng

Members: Sunil Madhow, Samyak Karnavat, Erchi Wang, Brandon Hsu

## Experiments

The purpose of the experiments is to compare the accuracy and runtime of methods performed with/without rNLA.

- [Approximate Matrix Multiplication](matrix_mul.ipynb)
- [Randomized Singular Value Decomposition](rsvd.ipynb)
- [Image Compression](ImageCompress.ipynb)

> [!NOTE]
> Libraries in [requirements.txt](requirements.txt) must be installed __before__ running any of the experiments/notebooks


## Results

### [Approximate Matrix Multiplication](matrix_mul.ipynb)

These experiments implement two versions of randomized matrix multiplication. One uses subsampling with uniform weights, and one uses subsampling with optimal weights. We compare the runtime of randomized matrix multiplication with that of numpy's built in matrix multiplication functionality. We also compare the error of each approximation scheme with respect to the output of numpy's built in matrix multiplication function. The results below can be obtained by running the jupyter notebook [matrix_mul.ipynb](matrix_mul.ipynb), provided that the libraries in [requirements.txt](requirements.txt) are installed. The whole notebook should take roughly a few minutes to run.

#### Runtime

![Mat mul runtimes](https://github.com/bhdsc/rNLA/blob/main/visualizations/exp1_times.png)

#### Errors

![Mat mul errors](https://github.com/bhdsc/rNLA/blob/main/visualizations/exp1_errors.png)


### [Randomized Singular Value Decomposition](rsvd.ipynb)

We evaluate and compare the low-rank approximation runtimes and errors for rSVD and SVD on square ($m=n$), tall ($m>n$), and fat ($m<n$) $R^{mxn}$ random matrices. Each row represents a unique data matrix to be approximated with a rank-k matrix produced by either rSVD or SVD. The first column of each row shows the sorted singular values for the matrix; the second column shows the rank-k approximation error for different values of k; the third column shows the runtime in seconds required to perform the rank-k approximation for different values of k; and the fourth column shows the speedup gained by performing rSVD instead of SVD ($runtime_{SVD} / runtime_{rSVD}$) for different values of k.

![m=n](https://github.com/bhdsc/rNLA/blob/main/visualizations/exp2_m=n.png)

![m>n](https://github.com/bhdsc/rNLA/blob/main/visualizations/exp2_m>n.png)

![m<n](https://github.com/bhdsc/rNLA/blob/main/visualizations/exp2_m<n.png)

_The results above are obtained by running the jupyter notebook [rsvd.ipynb](rsvd.ipynb) and took roughly 1.5 minutes to run on an entry level laptop._

### [Image Compression](ImageCompress.ipynb)

We evaluate the performance between rSVD and SVD on an image compression task. The code and complete results are included in [ImageCompress.ipynb](ImageCompress.ipynb).

#### Runtime

![Img_compress runtimes](https://github.com/bhdsc/rNLA/blob/main/visualizations/exp3_time.png)

#### Accuracy

We use two metrics: structural similarity index measure (SSIM) and peak signal-to-noise ratio (PSNR). Relative accuracy is reported as rSVD performs similar to SVD. 
$`\text{Relative Acc} = \frac{|\text{Acc(rSVD)}-\text{Acc(SVD)}|}{\text{Acc{SVD}}}`$

![Img_compress accuracies](https://github.com/bhdsc/rNLA/blob/main/visualizations/exp3_acc.png)

## References

For a full list of references, see our [report](README.md).
