#include<bits/stdc++.h>

using namespace std;
const int n=5;          //change value of n over here
int calFit(int m,int a[][n],int b[]){
    int i=0,fitness=0;
    for(i=0;i<n;i++){
        fitness=fitness+abs(b[i]-b[a[m][i]]);
    }
    return fitness;
}

int main() {
    int p,q,r,s,k;
    int array[n];
    int c[4][n];
    int b[4][n];
    cout<<"enter n values\n";
    for(int i=0;i<n;i++) cin>>array[i];

    for(int i=0;i<n;i++) b[0][i]=rand()%3;
    for(int i=0;i<n;i++) b[1][i]=rand()%3;
    for(int i=0;i<n;i++) b[2][i]=rand()%3;
    for(int i=0;i<n;i++) b[3][i]=rand()%3;
    p=calFit(0,b,array);
    q=calFit(1,b,array);
    r=calFit(2,b,array);
    s=calFit(3,b,array);
    cout<<p<<endl<<q<<endl<<r<<endl<<s<<endl;
    for(k=2;k<n-1;k++){
    for(int i=0;i<n;i++){
        c[0][i]=b[0][i];
        c[1][i]=b[1][i];
    }
    for(int i=0;i<k;i++){
        b[0][i]=c[0][i];
        b[1][i]=c[1][i];
    }
    for(int i=k;i<n;i++){
        b[0][i]=c[1][i];
        b[1][i]=c[0][i];
    }

    b[0][3]=2;b[1][3]=1;

    if(calFit(0,b,array )>p||calFit(1,b,array )>q||calFit(0,b,array )>q||calFit(1,b,array )>p)
     break;
    if(calFit(0,b,array )<p&&calFit(1,b,array )<q&&calFit(0,b,array )<q||calFit(1,b,array )<p)
     p=calFit(0,b,array );
     q=calFit(1,b,array );
    }

    for(k=2;k<n-1;k++){
    for(int i=0;i<n;i++){
        c[2][i]=b[2][i];
        c[3][i]=b[3][i];
    }
    for(int i=0;i<k;i++){
        b[2][i]=c[2][i];
        b[3][i]=c[3][i];
    }
    for(int i=k;i<n;i++){
        b[2][i]=c[3][i];
        b[3][i]=c[2][i];
    }
    b[2][3]=2;
    b[3][3]=1;
    if(calFit(2,b,array )>r||calFit(3,b,array )>s||calFit(2,b,array )>s||calFit(3,b,array )>r)
     break;
    if(calFit(2,b,array )<r&&calFit(3,b,array )<s&&calFit(2,b,array )<s||calFit(3,b,array )<r){
     p=calFit(0,b,array );
     q=calFit(1,b,array );
    }
    }
    for(int x=0;x<4;x++){
        if((calFit(x,b,array )<=calFit((x+1)%4,b,array ))&&(calFit(x,b,array )<=calFit((x+2)%4,b,array ))&&(calFit(x,b,array )<=calFit((x+3)%4,b,array ))&&(calFit(x,b,array )<=calFit(0,c,array ))&&(calFit(x,b,array )<=calFit(1,c,array ))&&(calFit(x,b,array )<=calFit(2,c,array ))&&(calFit(x,b,array )<=calFit(3,c,array ))){
        for(int i=0;i<n;i++){
            cout<<b[x][i]<<" ";
        }
        cout<<calFit(x,b,array );
        break;
        }
    }
    for(int x=0;x<4;x++){
        if((calFit(x,c,array )<=calFit((x+1)%4,c,array ))&&(calFit(x,c,array )<=calFit((x+2)%4,c,array ))&&(calFit(x,c,array )<=calFit((x+3)%4,c,array ))&&(calFit(x,c,array )<=calFit(0,b,array ))&&(calFit(x,c,array )<=calFit(1,b,array ))&&(calFit(x,c,array )<=calFit(2,b,array ))&&(calFit(x,c,array )<=calFit(3,b,array ))){
        for(int i=0;i<n;i++){
            cout<<c[x][i]<<" ";
        }
        cout<<calFit(x,c,array );
        break;
        }
    }
return 0;
}
