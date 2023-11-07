[BLACKBOARD GAME](https://codeforces.com/gym/104736/problem/B)
```c++
#include <bits/stdc++.h>

#define ll long long

using namespace std;

char solve(map<int,int>freq){
    for(auto &a : freq){
        if(a.second % 3) return 'Y';
    }
    
    return 'N';
}

int main(){
    int n; 
    cin>>n;
    
    vector<ll>nums(3*n);
    map<int,int>freq;
    
    for(int i = 0; i < 3*n; i++){
        cin>>nums[i];
        freq[nums[i]] ++;
    }
    
    cout<<solve(freq);
    
    return 0;
}
```
