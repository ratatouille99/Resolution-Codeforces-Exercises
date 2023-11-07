[Negatives and Positives](https://codeforces.com/contest/1791/problem/E)
```c++
#include <bits/stdc++.h>
#define ll long long

using namespace std;

int main(){
    int t, n;
    cin>>t;
    
    while(t--){
        cin >> n;
        vector<ll>a(n);
        ll cnt = 0, mn = 2e9, sum = 0;
        
        for (ll i=0;i<n;i++)
        {
            cin >> a[i];
            
            if (a[i] < 0) cnt++;
            
            mn = min(mn, abs(a[i]));
            
            sum += abs(a[i]);
        }
        
        if (cnt & 1) sum -= 2 * mn;
        
        cout << sum << "\n";

    }
    
    return 0;
}
```
