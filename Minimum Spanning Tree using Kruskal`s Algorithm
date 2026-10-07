#include <stdio.h>
#include <stdlib.h>
#include <limits.h>



void kruskalMST(int **cost, int V) {

	// Write your code here...
int parent[100];
    int mincost = 0;

    for (int i = 0; i < V; i++)
        parent[i] = i;

    int edge = 0;

    while (edge < V - 1)
    {
        int min = INT_MAX;
        int a = -1, b = -1;

        for (int i = 0; i < V; i++)
        {
            for (int j = i + 1; j < V; j++)
            {
                if (cost[i][j] < min)
                {
                    int x = i;
                    while (parent[x] != x)
                        x = parent[x];

                    int y = j;
                    while (parent[y] != y)
                        y = parent[y];

                    if (x != y)
                    {
                        min = cost[i][j];
                        a = i;
                        b = j;
                    }
                }
            }
        }

        int x = a;
        while (parent[x] != x)
            x = parent[x];

        int y = b;
        while (parent[y] != y)
            y = parent[y];

        parent[x] = y;

        printf("Edge %d:(%d, %d) cost:%d\n", edge, a, b, min);

        mincost += min;
        edge++;
    }

    printf("Minimum cost= %d\n", mincost);
}


int main() {
    int V;
    printf("No of vertices: ");
    scanf("%d", &V);

    int **cost = (int **)malloc(V * sizeof(int *));
    for (int i = 0; i < V; i++)
        cost[i] = (int *)malloc(V * sizeof(int));

    printf("Adjacency matrix:\n");
    for (int i = 0; i < V; i++)
        for (int j = 0; j < V; j++)
            scanf("%d", &cost[i][j]);

    kruskalMST(cost, V);

    for (int i = 0; i < V; i++)
        free(cost[i]);
    free(cost);

    return 0;
}
