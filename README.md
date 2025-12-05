#include <stdio.h>

int main() {
    int m, n;

    // Step 1: Read matrix dimensions
    printf("Enter number of rows (m): ");
    scanf("%d", &m);
    printf("Enter number of columns (n): ");
    scanf("%d", &n);

    int A[m][n], B[m][n], C[m][n];

    // Step 2: Read matrix A
    printf("Enter elements of matrix A:\n");
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < n; j++) {
            scanf("%d", &A[i][j]);
        }
    }

    // Step 3: Read matrix B
    printf("Enter elements of matrix B:\n");
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < n; j++) {
            scanf("%d", &B[i][j]);
        }
    }

    // Step 4: Compute difference C = A - B
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < n; j++) {
            C[i][j] = A[i][j] - B[i][j];
        }
    }

    // Step 5: Print result
    printf("Difference of matrices (A - B):\n");
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < n; j++) {
            printf("%d ", C[i][j]);
        }
        printf("\n");
    }

    return 0;
}
