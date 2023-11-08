# [Anonymoys Informant](https://codeforces.com/contest/1894/problem/C)
```c++
#include <bits/stdc++.h>

using namespace std;

int n, k;
int b[200010];
bool vis[200010];

void solve() {
    cin >> n >> k;
    for (int i = 1; i <= n; i++) {
        cin >> b[i];
    }
    for (int i = 1; i <= n; i++) {
        vis[i] = false;
    }

    unordered_set<int> s;
    int cur = n;
    bool ok = true;
    for (int i = 1; i <= k; i++) {
        if (b[cur] <= n) {
            if (vis[cur]) {
                break;
            } else {
                vis[cur] = true;
            }
            cur = ((cur - b[cur]) % n + n) % n;
            if (cur == 0) { cur = n; }
        } else {
            ok = false;
            break;
        }
    }

    cout << (ok ? "Yes\n" : "No\n");
}

int main() {
    ios_base::sync_with_stdio(false);
    cin.tie(nullptr);

    int t;
    cin >> t;
    for (int i = 1; i <= t; i++) {
        solve();
    }
}
```
