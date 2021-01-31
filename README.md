#include <stdio.h>
#include <cs50.h>

int main(void)
{
    // Get integer from user between 1 and 8 inclusive
    int n;
    do
    {
        n = get_int("Height: ");
    }
    while (n > 8 || n < 1);

    // Create n rows of bricks
    for (int i = 0; i < n; i++)
    {
        // Print " " (n - 1 - i) times basically for mario bricks
        for (int d = n - 1; d > i; d--)
        {
            printf(" ");
        }

        // Print '#' (i + 1) times basically for mario bricks
        for (int h = -1; h < i; h++)
        {
            printf("#");
        }
        printf("\n");
    }
}
