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
    printf("\nStep 1 :-\n");
    for (j = 2; j <= n; j++)
    {
        i = 1;
        while (a[j] > a[i])
        {
            i++;
        }
        temp = a[j];


// ----------    loop of i shown in output ------------------------
        printf("after i[%d] loop = ", i);
        for (c = 1; c <= n; c++)
        {
            printf("%d ", a[c]);
        }
        printf("\tTemp=%d\n", temp);
// -------------- end -----------------------------------

        for (k = 0; k <= (j - i - 1); k++)
        {
            a[j - k] = a[j - k - 1];

// ----------    loop of k shown in output ------------------------
            printf("after k[%d] loop = ", k);
            for (c = 1; c <= n; c++)
            {
                printf("%d ", a[c]);
            }
            printf("\tTemp=%d\n", temp);
// ------------------ end ----------------------------------

        }
        a[i] = temp;


// ----------    loop of k shown in output ------------------------
            printf("AFTER J[%d] LOOP = ", j);
            for (c = 1; c <= n; c++)
            {
                printf("%d ", a[c]);
            }
            printf("\tTemp=%d ---------\n\n\nStep %d :-\n", temp,j);
// ------------------ end ----------------------------------
      
    }
    printf("Ascending order is\t");
    for (c = 1; c <= n; c++)
    {
        printf("%d ", a[c]);
    }
    return 0;
}
