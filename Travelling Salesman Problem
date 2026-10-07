#include <stdio.h>

#define INF 999999

int n;
int cost[20][20];
int visited[20];
int minCost = INF;

void tsp(int current, int count, int totalCost)
{
    if (count == n)
    {
        /* Return to starting city */
        if (cost[current][0] != -1)
        {
            int finalCost = totalCost + cost[current][0];

            if (finalCost < minCost)
                minCost = finalCost;
        }
        return;
    }

    for (int next = 0; next < n; next++)
    {
        if (!visited[next] && cost[current][next] != -1)
        {
            visited[next] = 1;

            tsp(next, count + 1,
                totalCost + cost[current][next]);

            visited[next] = 0;
        }
    }
}

int main()
{
    scanf("%d", &n);

    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < n; j++)
        {
            scanf("%d", &cost[i][j]);
        }
    }

    for (int i = 0; i < n; i++)
        visited[i] = 0;

    /* Start from city 1 (index 0) */
    visited[0] = 1;

    tsp(0, 1, 0);

    printf("%d\n", minCost);

    return 0;
}
