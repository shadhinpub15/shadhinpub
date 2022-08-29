#include<stdio.h>
int main()
{
    int arr[1000],n,size,search,first,middle,last,i;
    printf("Input array size of n: ");
    scanf("%d",&n);
    printf("Input array element: ");
    for(i=1;i<=n;i++)
    {
        scanf("%d",&arr[i]);
    }
    printf("Input Searching number: ");
    scanf("%d",&search);
    first=0;
    last=n-1;
    middle=(first+last)/2;
    while( first <= last )
    {
        if( arr[middle] < search)
            first= middle+1;
        else if( arr[middle] == search)
        {
            printf("%d is present in index no: %d.\n",search,middle+1);
            break;
        }
        else
      last= middle-1;
      middle= (first+last)/2;
    }
    if(first>last)
    {
        printf("%d The searching number is not found",search,size);
    }
    return 0;
}
