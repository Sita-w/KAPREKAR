#include<stdio.h>
int main()
{
	int n,a,b,c,i,s,m;
	scanf("%d",&n);
	a=n%10;
    b=n/10%10;
    c=n/100;
	if(a==b&&a==c)
	    {
	    	printf("1:%d-%d=0",n,n);
	    	return 0;
	    }
	if(n==495)
	printf("1: 954 - 459 = 495\n");
	for(i=1;n!=495;i++)
	{
		a=n%10;
	    b=n/10%10;
	    c=n/100; 
    	if(a>=b&&a>=c&&b>=c)
    	{
		    s=a*100+b*10+c;
            m=c*100+b*10+a;	
		}
		else if(a>=b&&a>=c&&c>=b)
		{
			s=a*100+c*10+b;
            m=b*100+c*10+a;
		}
		else if(b>=a&&b>=c&&a>=c)
		{
			s=b*100+a*10+c;
            m=c*100+a*10+b;
		}
		else if(b>=a&&b>=c&&c>=a)
		{
			s=b*100+c*10+a;
            m=a*100+c*10+b;
		}
		else if(c>=a&&c>=b&&a>=b)
		{
			s=c*100+a*10+b;
            m=b*100+a*10+c;
		}
		else if(c>=a&&c>=b&&b>=a)
		{
			s=c*100+b*10+a;
            m=a*100+b*10+c;
		}
	    n=s-m;
		printf("%d: %d - %d = %d\n",i,s,m,n);	
	}
	return 0;
}
