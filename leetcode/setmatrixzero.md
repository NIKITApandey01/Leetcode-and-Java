Given an m x n integer matrix matrix, if an element is 0, set its entire row and column to 0's.

You must do it in place.

 

Example 1:


Input: matrix = [[1,1,1],[1,0,1],[1,1,1]]
Output: [[1,0,1],[0,0,0],[1,0,1]]
Example 2:


Input: matrix = [[0,1,2,0],[3,4,5,2],[1,3,1,5]]
Output: [[0,0,0,0],[0,4,5,0],[0,3,1,0]]
 

Constraints:

m == matrix.length
n == matrix[0].length
1 <= m, n <= 200
-231 <= matrix[i][j] <= 231 - 1



    boolean isCol = false;
    int R = matrix.length;
    int C = matrix[0].length;

    for (int i = 0; i < R; i++) {
        if (matrix[i][0] == 0) {
            isCol = true;
        }
        for (int j = 1; j < C; j++) {
            if (matrix[i][j] == 0) {
                matrix[i][0] = 0;
                matrix[0][j] = 0;
            }
        }
    }
    for (int i = 1; i < R; i++) {
        for (int j = 1; j < C; j++) {
            if (matrix[i][0] == 0 || matrix[0][j] == 0) {
                matrix[i][j] = 0;
            }
        }
    }

    if (matrix[0][0] == 0) {
        for (int j = 0; j < C; j++) {
            matrix[0][j] = 0;
        }
    }
    if (isCol) {
        for (int i = 0; i < R; i++) {
            matrix[i][0] = 0;
        }
    }



This code is solving the problem of setting all the elements in a given matrix to zero if any element in the matrix is zero.
The approach is using the first row and first column as markers to store information about which row and columns needs to be set to zero.

The first line initializes a boolean variable isCol to false, this variable is used later to check if the first column needs to be set to zero.

The next two lines store the number of rows (R) and columns (C) in the matrix.

The first nested loop iterates over all the rows and columns, starting from the second column (j=1).

If an element in the matrix is zero, it sets the corresponding element in the first column and first row to zero.
If an element in the first column is zero, it sets the isCol variable to true.
The next nested loop iterates over all the rows and columns, again starting from the second column and row.

If an element in the first column or first row is zero, it sets the corresponding element in the matrix to zero.
The next two lines check if the first element of the first row or first column is zero. If it is, it sets the entire first row or first column to zero.

Overall, this code uses the first row and column of the matrix to store information about which rows and columns need to be set to zero and uses that information to set the appropriate elements in the matrix to zero. This allows the solution to be done in-place and have a O(1) space complexity.



