#include <stdio.h>

int main()
{
    int N, W;

    scanf("%d", &N);

    int value[N], weight[N];

    for (int i = 0; i < N; i++)
        scanf("%d", &value[i]);

    for (int i = 0; i < N; i++)
        scanf("%d", &weight[i]);

    scanf("%d", &W);

    int dp[W + 1];

    for (int j = 0; j <= W; j++)
        dp[j] = 0;

    for (int i = 0; i < N; i++)
    {
        for (int j = W; j >= weight[i]; j--)
        {
            int include = value[i] + dp[j - weight[i]];

            if (include > dp[j])
                dp[j] = include;
        }
    }

    printf("%d\n", dp[W]);

    return 0;
}
