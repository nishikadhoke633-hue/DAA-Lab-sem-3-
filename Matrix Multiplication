#include <stdio.h>

int main() {
    int m, n, n2, p;

    // Dimensions of matrix A
    scanf("%d %d", &m, &n);

    int A[m][n];

    // Read matrix A
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < n; j++) {
            scanf("%d", &A[i][j]);
        }
    }

    // Dimensions of matrix B
    scanf("%d %d", &n2, &p);

    // Check multiplication condition
    if (n != n2) {
        printf("Invalid input");
        return 0;
    }

    int B[n2][p];
    int C[m][p];

    // Read matrix B
    for (int i = 0; i < n2; i++) {
        for (int j = 0; j < p; j++) {
            scanf("%d", &B[i][j]);
        }
    }

    // Matrix multiplication
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < p; j++) {
            C[i][j] = 0;

            for (int k = 0; k < n; k++) {
                C[i][j] += A[i][k] * B[k][j];
            }
        }
    }

    // Print result
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < p; j++) {
            printf("%d ", C[i][j]);
        }
        printf("\n");
    }

    return 0;
}
