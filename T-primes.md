[T-primes](https://codeforces.com/contest/230/problem/B)
```c++
#include <bits/stdc++.h>

using namespace std;

#define ll long long

bool isPrime(ll x){
    for(int i = 2; i <= sqrt(x); i++){
        if(x % i == 0) return false;
    }
    
    return true;
}

int main()
{
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);
    cout.tie(NULL);
    
    ll n = 0, cnt = 0, x = 0;
    
    cin>>n;
    
    for(ll i = 0; i < n; i++){
        cin>>x;
        
        cnt = sqrt(x);
        
        if(x > 1 && cnt * cnt == x && isPrime(cnt)) cout<<"YES\n";
        else cout<<"NO\n";
    }

    return 0;
}
```

```
