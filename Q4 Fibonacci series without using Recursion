#include <stdio.h>

int main()
{
    int i, n, firstTerm=0, secondTerm=1, sum=0;
    printf("\nEnter number of terms required in Fibonacci Series: ");
    scanf("%d",&n);
    
    printf("\nFibonacci Series is:\n\n\n %d %d ", firstTerm, secondTerm); 
    i=2;    
    while (i<n)
    {
        sum=firstTerm+secondTerm;
        firstTerm=secondTerm;
        secondTerm=sum;
        ++i;
        printf("%d ",sum);
    }
    return 0;
}
