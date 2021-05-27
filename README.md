# 234
233
void invert(int a[],int n)
{
  int i,w,nn = n/2;
  for(i=0;i<=nn;i++)
  {
    w = a[i];
	a[i] = a[n-1-i];
	a[n-1-i] = w;
  }
}

int main()
{
   int i,n,*a;
   while(1)
   {
      printf("enter n:");
      scanf("%d",&n);
      printf("\n");
      if(n>0)
        break;
   }
   a = (int *)malloc(sizeof(int)*n);
   if(a==0)
   {
      printf("allocation error_aborting");
      exit(1);
   }

   printf("enter a[0]....a[%d]:",n-1);
   for(i=0;i<n;i++)
      scanf("%d",a++);
   invert(a-n,n);
  printf("the array has been invert:\n");
  for(i=0;i<n;i++)
  {
     if(i%5==0)
		 printf("\n");
      printf("%5d",*(a-n+i));
  }
    return 0;
}
