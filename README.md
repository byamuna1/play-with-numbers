# play-with-numbers
#include <iostream>
 
using namespace std;
 
int main() {
	int n,m;
	cin>>n>>m;
	long int a[n];
	long long int sum[n],sum1=0;
	for(int i=0;i<n;i++)
	{
	    cin>>a[i];
	    sum1+=a[i];
	    sum[i]=sum1;
	}
	
	while(m--)
	{
	    int L,R;
	    cin>>L>>R;
	    if(L==1)
	    cout<<sum[R-1]/R<<"\n";
	    else
	    {
	        cout<<(sum[R-1]-sum[L-2])/(R-L+1)<<"\n";
	    }
	}
}
