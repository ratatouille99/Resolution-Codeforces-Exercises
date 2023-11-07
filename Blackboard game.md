[FOOTBALL](https://codeforces.com/contest/96/problem/A)
```c++
#include <bits/stdc++.h>

using namespace std;

int main(){
    string s, zeros = "0000000", ones = "1111111";
    cin>>s;
    
    if(s.find(zeros) != string::npos  || s.find(ones) != string::npos) cout<<"YES";
    else cout<<"NO";
    
    return 0;
}
```
