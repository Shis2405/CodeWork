/*

    Time Complexity: O(N * M)
    Space Complexity: O(1)

    Where N, M are the number of rowStarts and the number of colStartumns of the matrix, 
    respectively. 

*/

import java.util.ArrayList;

public class Solution {

    public static void rotateMatrix(ArrayList<ArrayList<Integer>> mat, int n, int m) {
        // Index of starting row and column
        int rowStart = 0, colStart = 0;

        int previous, current;

        while (rowStart < n && colStart < m) {

            // If we have rotated the whole matrix
            if (rowStart == n - 1 || colStart == m - 1) {
                break;
            }
            previous = mat.get(rowStart + 1).get(colStart);

            // Move elements of first row from the remaining rows
            for (int i = colStart; i < m; i++) {

                current = mat.get(rowStart).get(i);
                mat.get(rowStart).set(i, previous);
                previous = current;
            }

            rowStart++;

            // Move elements of last column from the remaining columns
            for (int i = rowStart; i < n; i++) {

                current = mat.get(i).get(m - 1);
                mat.get(i).set(m - 1, previous);
                previous = current;
            }
            m--;

            // Move elements of last row from the remaining rows
            if (rowStart < n) {
                for (int i = m - 1; i >= colStart; i--) {
                    current = mat.get(n - 1).get(i);
                    mat.get(n - 1).set(i, previous);
                    previous = current;
                }
            }
            n--;

            // Move elements of first column from the remaining rows
            if (colStart < m) {
                for (int i = n - 1; i >= rowStart; i--) {
                    current = mat.get(i).get(colStart);
                    mat.get(i).set(colStart, previous);
                    previous = current;
                }
            }
            colStart++;

        }

    }

}
