#include<stdio.h>
int main()
{
    int a[20],i,n,j,temp=0,first,last,key,mid;
    printf("enter the number of elements\n");
    scanf("%d",&n);
    
    printf("enter %d elements\n",n);
    for(i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=0;i<n-1;i++)
    {
        for(j=0;j<n-1-i;j++)
        {
            if(a[j]>a[j+1])
            {
                temp=a[j];
                a[j]=a[j+1];
                a[j+1]=temp;
            }
        }
    }
    printf("the sorted array is.....\n");
    for(i=0;i<n;i++)
    {
        printf("%d\t",a[i]);
    }
    printf("\n");
    
    
    
    
    printf("enter a key\n");
    scanf("%d",&key);
    
    first=0;
    last=n-1;
    while(first<=last)
    {
        mid=first+last/2;
        if(a[mid]==key)
        {
        printf("key %d is found at %d location\n",key,mid+1);
        return 0;
        }
    
  else if(key<a[mid])
    {
        last=mid-1;
    }
    else
    {
        first=mid+1;
    }
    printf("key %d is not found at the location\n",key);
    
    return 1;
      }
  }
    

