### Why Rows for One Matrix and Columns for Another in Matrix Multiplication

#### The Math Behind Matrix Multiplication

When you multiply two matrices \( A \) and \( B \), to obtain element \( C[i, j] \) in the resultant matrix \( C \), you need to calculate the dot product of the \( i^{th} \) row from \( A \) with the \( j^{th} \) column of \( B \).

\[ C[i, j] = \text{dot}(A[i, :], B[:, j]) \]

In simple terms, the \( i^{th} \) row of \( A \) and the \( j^{th} \) column of \( B \) are aligned such that the \( k^{th} \) element in the row of \( A \) is multiplied by the \( k^{th} \) element in the column of \( B \), and all these products are summed together to yield \( C[i, j] \).

#### Why Not Rows for Both or Columns for Both?

While mathematically possible to define other forms of multiplications (like Hadamard product), the standard matrix multiplication is defined this way. This definition leverages both the row-wise and column-wise structures of the matrices involved. This makes it compatible with a variety of mathematical applications like solving systems of equations, network flow problems, and even in computing graph algorithms in linear algebraic representation.

#### Practical Benefits

In linear algebra libraries and even in hardware, this specific form of matrix multiplication is highly optimized. For instance, certain matrix multiplication algorithms such as Strassen's algorithm or the Coppersmith–Winograd algorithm exploit this row-column relationship to accelerate multiplication.

In your asynchronous I/O context, you fetched rows from one matrix and columns from the other so you could perform many dot product operations in parallel, thereby making effective use of asynchronous programming paradigms.

So, in summary, it's not an arbitrary choice; it's both mathematically justified and practically beneficial to take rows from one matrix and columns from another when performing matrix multiplication.