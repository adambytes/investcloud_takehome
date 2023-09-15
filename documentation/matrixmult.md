### Matrix Multiplication Explained

Matrix multiplication, often denoted by a dot product in NumPy, is a fundamental operation in linear algebra. The idea is that you take the rows from the first matrix and do a dot product with the columns from the second matrix, populating the resultant matrix with the sums. The dimensions must be compatible for multiplication to be performed. Specifically, if you have a matrix A with dimensions `(m, n)` and another matrix B with dimensions `(p, q)`, then `n` should be equal to `p` for the multiplication to be valid. The resultant matrix C will have dimensions `(m, q)`.

#### Given matrices A and B

Let's say `A` and `B` are both 3x3 matrices. 

- \( A = \begin{pmatrix}
  a_{11} & a_{12} & a_{13} \\
  a_{21} & a_{22} & a_{23} \\
  a_{31} & a_{32} & a_{33}
  \end{pmatrix} \)

- \( B = \begin{pmatrix}
  b_{11} & b_{12} & b_{13} \\
  b_{21} & b_{22} & b_{23} \\
  b_{31} & b_{32} & b_{33}
  \end{pmatrix} \)

#### Resultant matrix C

The resultant matrix `C` will also be a 3x3 matrix.

- \( C = \begin{pmatrix}
  c_{11} & c_{12} & c_{13} \\
  c_{21} & c_{22} & c_{23} \\
  c_{31} & c_{32} & c_{33}
  \end{pmatrix} \)

#### Multiplication rules

To get each element \( c_{ij} \) in `C`, you take the dot product of the ith row from `A` and the jth column from `B`.

For example, to compute \( c_{11} \):

- \( c_{11} = a_{11}*b_{11} + a_{12}*b_{21} + a_{13}*b_{31} \)

To compute \( c_{12} \):

- \( c_{12} = a_{11}*b_{12} + a_{12}*b_{22} + a_{13}*b_{32} \)

And so on for each element of the resultant matrix `C`.

### Summary

You'll loop through each row of matrix `A` and each column of matrix `B`, compute the dot product, and populate the corresponding cell in the resulting matrix `C`. That's essentially what your asynchronous code is doing: it fetches each row of the first matrix and each column of the second matrix to perform these computations.