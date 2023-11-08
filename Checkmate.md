#include <bits/stdc++.h>

using namespace std;

int main()
{
    ios_base::sync_with_stdio(false);
    cout.tie(NULL);
    
    vector<int>pens(3,0), aux(3,0);
    int contador = 0;
    string words{}; 

    if (cin >> pens[0] >> pens[1] >> pens[2]>>skipws)
    {
        cin>>ws;
        getline(cin, words,'\n');
    }
    
    for(int i = 0; i < words.length(); i++){
        if(tolower(words[i]) >= 'a' && tolower(words[i]) <= 'z') aux[0]++;
        else if(isdigit(words[i]) > 0) aux[1]++;
        else if(words[i] != ' ') aux[2]++;
    }
    
    sort(aux.begin(), aux.end());
    sort(pens.begin(), pens.end());
    
    if(pens[0] >= aux[0] && pens[1] >= aux[1] && pens[2] >= aux[2]) cout<<"Yes";
    else cout<<"No";
    
    return 0;
}
