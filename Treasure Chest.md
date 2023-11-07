[Treasure Chest](https://codeforces.com/contest/1895/problem/A)
```c++
#include <bits/stdc++.h>

#define ll long long

using namespace std;

int main(){
    int t;
    cin>>t;
    
    while(t--){
        int x{}, y{}, k{};
        
        cin>>x>>y>>k;
        
        if(x >= y) cout<<x<<'\n';
        else if(y - x <= k && y > x) cout<<y<<'\n';
        else cout<< y + (y - (x + k))<<'\n';
    }
    
    return 0;
}
```
