#include<stdio.h>
#include<math.h>
void main()
{
    float a[10],*ptr,sum=0,mean=0;
    float sumstd=0,var=0;
    int i,n;
    printf("enter the number of elements:\n");
    scanf("%d",&n);
    printf("enter the elements of araay:\n");
    for(i=0;i<n;i++)
        {
            scanf("%f",&a[i]);
        }
    ptr=a;
    for(i=0;i<n;i++)
        {
            sum=sum+*ptr;
            ptr++;
        }
    mean=sum/n;
    ptr=a;
    for(i=0;i<n;i++)
        {
            sumstd+=(*ptr-mean)*(*ptr-mean);
            ptr++;
        }
    var=sumstd/n;
    float std=sqrt(var);
    printf("sum:%0.3f\n",sum);
    printf("mean:%0.3f\n",mean);
    printf("variance:%0.3f\n",var);
    printf("standard deviation:%0.3f\n",std);
}
