[Secret Sport](https://codeforces.com/contest/1894/problem/B)
```c++
#include <iostream>
#include <unordered_map>
using namespace std;

int n, a[110];

void solve() {
    cin >> n;
    for (int i = 1; i <= n; i++) {
        cin >> a[i];
    }

    unordered_map<int, int> freq;
    int can = 0;
    for (int i = 1; i <= n; i++) {
        if (++freq[a[i]] == 2) {
            can++;
        }
    }

    if (can < 2) {
        cout << -1 << '\n';
        return;
    }

    int n12 = 0, n13 = 0;
    for (auto [v, f] : freq) {
        if (f >= 2) {
            if (n12 == 0) { n12 = v; }
            else { n13 = v; break; }
        }
    }

    for (int i = 1; i <= n; i++) {
        if (a[i] == n12) {
            cout << 2 << ' ';
            n12 = 0;
        } else if (a[i] == n13) {
            cout << 3 << ' ';
            n13 = 0;
        } else {
            cout << 1 << ' ';
        }
    }
    cout << '\n';
}

int main() {
#ifdef ONLINE_JUDGE
    ios_base::sync_with_stdio(false);
    cin.tie(nullptr);
#endif

    int t;
    cin >> t;
    for (int i = 1; i <= t; i++) {
        solve();
    }
}
```
