# HackerRAnk-Birthday-Candles
Colleen is turning  years old! Therefore, she has  candles of various heights on her cake, and candle  has height . Because the taller candles tower over the shorter ones, Colleen can only blow out the tallest candles.  Given the  for each individual candle, find and print the number of candles she can successfully blow out.
#######################################################################################################
#include<stdio.h>
int main()
{
	int i,n=0,b=0,count=1,A[100];
	scanf("%d",&n);
for(int i=0;i<n;i++)
{
	scanf("%d",&A[i]);
}
for(int j=0;j<n;j++)
{
	for(int k=j+1;k<n;k++)
	{
	if(A[j]<A[k])
	{
		b=A[k];
		A[k]=A[j]; 
		A[j]=b;
	}
}
	}
	for(int l=1;l<n;l++)
	{
		if(A[0]==A[l]){
		
		count++;}
	}
	/*for(int q=0;q<n;q++)
	{
		printf("%d",A[q]);
	}*/
	printf("%d",count);
	return 0;
}
