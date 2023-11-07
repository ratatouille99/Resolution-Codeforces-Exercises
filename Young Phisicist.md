[YOUNG PHISICIST](https://codeforces.com/contest/69/problem/A)
```c++
#include<bits/stdc++.h>

#define ll long long

using namespace std;

int main(){
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);
    cout.tie(NULL);
    
    ll x = 0, y = 0, z = 0;

    int n; 
    
    cin>>n;
    
    for(int i = 0; i < n; i++){
        ll aux1 = 0, aux2 = 0, aux3 = 0;
        cin>>aux1>>aux2>>aux3;
        
        x+=aux1;
        y+=aux2;
        z+=aux3;
    }
    
    if(x != 0 || y != 0 || z != 0) cout<<"NO";
    else cout<<"YES";
    
    return 0;
}
```
