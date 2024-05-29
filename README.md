# CODEFORCES MIKE AND STRINGS
<div align="center">
  <h1>Título de mi Proyecto</h1>
  <img src="https://github.com/AnndyyRobles/B.-Mike-and-strings-approach/blob/main/imgs/img1.jpg" alt="problem" width="500" style="border-radius: 15px;"/>
</div>

```cpp
#include<bits/stdc++.h>
using namespace std;
#define LightningSpeed ios_base::sync_with_stdio(0); cin.tie(0); cout.tie(0);
#define ll long long 
#define all(v) v.begin(),v.end()
#define rall(v) v.rbegin(),v.rend()
#define getunique(v) {sort(all(v)); v.erase(unique(all(v)), v.end());}
#define readv(x, n) vc x(n); asc(i,n) cin>>x[i];
#define asc(i,n) for(int i=0;i<n;i++)
#define asc1(i,n) for(int i=1;i<=n;i++)
#define desc(i,n) for(int i=1;i<=n;i++)
#define pb push_back
#define lb lower_bound
#define ub upper_bound

#define p_vec(x)      \
    for (auto &i : x)      \
        cout << i << ' '; \
    cout << endl;
    
#define len length()
#define nl "\n"
#define sz size()

#define rc(x) return cout<<x<<endl,0
const int inf = 2e9 + 1e8;

int main(){
    LightningSpeed
    int n; cin>>n;
    vector<string> strings(n);
    asc(i,n){
        cin>>strings[i];
    }
    int less = inf;
    for(string s : strings){
        int count = 0;
        asc(it,n){
            int i = 0;
            string mov = strings[it];
            while(i < mov.len && mov != s){
                mov += mov[0]; 
                mov.erase(0, 1);
                i++;
            }
            if(mov != s){
                cout<<"-1"<<nl;
                return 0;
            }
            count += i;
        }
        less = min(less, count);
    }
    cout<<less<<nl;
    return 0;
}
```
