[DECIPHERING WORDWHIZ](https://codeforces.com/gym/104736/problem/B)
```c++
#include <bits/stdc++.h>

#define ll long long

using namespace std;

string ans(map<char,int>&secret, string now){
    string res = "-----";
    
    for(int i = 0; i < 5; i++){
        char element = now[i];
        if(secret.count(element) > 0){
            if(secret[element] == i) res[i] = '*';
            else res[i] = '!';
        }
        
        else res[i] = 'X';
    }
    
    return res;
}

int main(){
    int n, g;
    vector<string>words, comp;
    map<char,int>secret;
    
    cin >> n;
    
    words.resize(n);
    comp.resize(n);
    
    cin>>words[0];
    
    for(int i = 0; i < 5; i++) secret[words[0][i]] = i;
    
    comp[0] =ans(secret, words[0]);
    
    for(int i = 1; i < n; i++){
        cin>>words[i];
        
        comp[i] = ans(secret, words[i]);
    }
    
    cin>>g;
    
    for(int i = 0; i < g; i++){
        string now {};
        int cont = 0;
        cin>>now;
        
        for(auto &a : comp){
            if(a == now) cont++;
        }
        
        cout<<cont<<'\n';
    }
    
    
    return 0;
}
```
