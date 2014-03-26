netflix-ALS-MPI
===============

Using alternating least squares and MPI to solve the Netflix Prize.

Lapacke和CBLAS的安装和使用

安装Lapacke时出现错误:
```
gfortran: error: ../../librefblas.a: No such file or directory
make[1]: *** [../xblat1s] Error 1
make[1]: Leaving directory `/home/onlyme/Downloads/lapack/BLAS/TESTING'
make: *** [blas_testing] Error 2
```
解决方法:
```
make blaslib #先编译blaslib
make lapacke #再编译lapacke
make lapacke_example #检查lapacke是否安装成功
g++ als_chow.cpp -llapack -lblas -o als #compile als with lapack and blas:
```
