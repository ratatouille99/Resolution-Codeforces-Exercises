[Secret Sport]((https://codeforces.com/contest/1894/problem/A))
```c++
#include <bits/stdc++.h>

using namespace std;

int main(){
    string mat{};
    vector<int>nums;
    
    cin>>mat;
    
    for(int i = 0; i < mat.length(); i+=2) nums.push_back(mat[i] - '0');
    
    sort(nums.begin(), nums.end());
    
    for(int i = 0, j = 0; i < nums.size(); i++, j+=2) mat[j] = nums[i] + '0';
    
    cout<<mat;
    
    return 0;
}
```
