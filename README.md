# cpp-template
/**

                              Online C++ Compiler.
               Code, Compile, Run and Debug C++ program online.
Write your code in this editor and press "Run" button to compile and execute it.

*/

#include <bits/stdc++.h>
#define ll long long 
using namespace std;

long long gcd(long long a,long long b){
    return b?gcd(b,a%b):a;
}

long long primechk[10000];

void preprocess(long long N){
    long long i,j;
    for(i=2;i<=N;i++){
        primechk[i]=1;
    }
    for(i=2;i<=N;i++){
        if(primechk[i]==1){
            for(j=2;i*j<=N;j++){primechk[i*j]=0;}
        }
    }
}

bool isPrime(int n) {
 
    if (n <= 1) return false;
    if (n <= 3) return true;
    if (n % 2 == 0 || n % 3 == 0) return false;
    for (int i = 5; i * i <= n; i = i + 6)
        if (n % i == 0 || n % (i + 2) == 0)
            return false;
    return true;
}

long long Binexpo(long long a,long long b){
    if(b==0)
        return 1;
    long long res=Binexpo(a,b/2);
    if(b%2){return res*res*a;}
    else{return res*res;}
}
long long Pwr(long long a,long long b,long long m){
    a%=m;
    long long res=1;
    while(b>0){
        if(b%2){res=res*a%m;}
        a=a*a%m;
        b>>=1;
    }
    return res;
}
int main()
{   long long a,b,c,d,e,f,g,h,i,j,k,x,y,z,sum=0,cnt=0,n,l,r,hi,lo,t,val=1;
    

    return 0;
}
