[WE WERE BOTH CHILDREN](https://codeforces.com/contest/1850/problem/F)
```c++
#include <bits/stdc++.h>
using namespace std;

#define ll long long

int main() {
  ios_base::sync_with_stdio(0);
  cin.tie(NULL);

  int t;
  cin >> t;
  
  while (t--) {
    ll n = 0, contador = 0;
    cin >> n;

    map<ll, ll> mapa, res;

    for (int i = 0; i < n; i++) {
      int x;
      cin>>x;
      mapa[x]++;
    }

    for (auto [a,b] : mapa) {
      for (int j = a; j <= n; j+=a) {
        res[j]+=b;
      }
    }

    for (auto &a : res)
      contador = max(contador,a.second);

    cout << contador << '\n';
  }

  return 0;
}
```
