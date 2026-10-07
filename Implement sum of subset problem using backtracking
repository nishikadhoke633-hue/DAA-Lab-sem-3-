#include <stdio.h>

int a[20], subset[20];
int n, target;
int found = 0;

int solutions[100][20];
int sizes[100];
int count = 0;

void backtrack(int index, int sum, int size)
{
    if (sum == target)
    {
        for (int i = 0; i < size; i++)
            solutions[count][i] = subset[i];

        sizes[count] = size;
        count++;
        found = 1;
        return;
    }

    if (index == n)
        return;

    /* Include current element */
    subset[size] = a[index];
    backtrack(index + 1, sum + a[index], size + 1);

    /* Exclude current element */
    backtrack(index + 1, sum, size);
}

int main()
{
    scanf("%d", &n);

    for (int i = 0; i < n; i++)
        scanf("%d", &a[i]);

    scanf("%d", &target);

    backtrack(0, 0, 0);

    if (!found)
    {
        printf("-1\n");
    }
    else
    {
        for (int i = count - 1; i >= 0; i--)
        {
            for (int j = 0; j < sizes[i]; j++)
            {
                printf("%d ", solutions[i][j]);
            }
            printf("\n");
        }
    }

    return 0;
}
