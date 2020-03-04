#include <stdio.h>
int main()
{
    int a[200], n, i, j, temp, c, k;
    printf("enter total number:");
    scanf("%d", &n);
    printf("enter elements:\n");
    for (c = 1; c <= n; c++)
    {
        scanf("%d", &a[c]);
    }
    printf("\nStep 1:-\n");
    for (j = 2; j <= n; j++)
    {
        i = 1;
        while (a[j] > a[i])
        {
            i++;
        }
        temp = a[j];
        printf("after i[%d] loop = %d %d %d %d %d\tTemp=%d\n", i, a[1], a[2], a[3], a[4], a[5], temp);
        for (k = 0; k <= (j - i - 1); k++)
        {
            a[j - k] = a[j - k - 1];

            printf("after k[%d] loop = %d %d %d %d %d\tTemp=%d\n", k, a[1], a[2], a[3], a[4], a[5], temp);
        }
        a[i] = temp;
        printf("after j[%d] loop = %d %d %d %d %d\tTemp=%d\n\n\nStep %d:-\n", j, a[1], a[2], a[3], a[4], a[5], temp, j);
    }
    printf("Ascending order is\t");
    for (c = 1; c <= n; c++)
    {
        printf("%d ", a[c]);
    }
    return 0;
}
