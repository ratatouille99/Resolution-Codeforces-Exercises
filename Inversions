[INVERSIONS](https://codeforces.com/gym/104736/problem/I)
```c++
#include<bits/stdc++.h>
#define i64 long long
using namespace std;
const int N = 1e6+10;
int h[26],Sm[N];
string s;
i64 k;
const int mod = 1e9+7;
void solve(){
	cin>>s>>k;
	int n=s.length();
	i64 ans=0;
	for(int i=n-1;i>=0;i--){
		for(int j=0;j+'a'<s[i];j++){
			ans+=h[j];
		}
		h[s[i]-'a']++;
	}
	i64 Sum=0;
	for(int i=0;i<n;i++){
		for(int j=0;j+'a'<s[i];j++){
			Sm[i]+=h[j];
		}
		Sum+=Sm[i];
	}
	cout<<(((ans%mod)*(k%mod))%mod+((Sum%mod)*(k%mod)%mod)*(((k-1)%mod)*500000004%mod))%mod<<"\n";
}
int main()
{
	ios::sync_with_stdio(false);
	cin.tie(),cout.tie();
	
	solve();
	
	return 0;
}
```
