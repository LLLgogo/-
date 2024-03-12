[](https://www.lanqiao.cn/courses/21965/learning/?id=1149557&compatibility=false)

`#include<bits/stdc++.h>`
`using namespace std;`
`int main()`
`{`
	`//测试用例的数量`
	`int t;`
	`cin>>t;`
	`//循环测试用例` 
	`while(t--)`
	`{`
		`int n;`
		`int k;`
		`//假设最大天数为1e4` 
		`int ans=1e4;`
		`vector<int> a;`
		`cin>>n>>k;`
		`for(int i=0;i<n;i++)`
		`{`
			`//输入每间房子的颜色` 
			`int x;`
			`cin>>x;`
			`//将每个房间的颜色加入容器中`
			`a.push_back(x);//vector的常用函数,用于在末尾添加` 
		`}`
		`//暴力枚举`
		`for(int i=1;i<=60;i++)`
		`{`
			`int res=0;`
			`for(int j=0;j<a.size();j++)//a.size()为vecor常用函数` 
			`{`
				`if(a[j]!=i)`
				`{`
					`res++;`
					`j=j+(k-1);`
				`}`
			`}`
			`ans=min(res,ans);`
		`}`
``	

		 cout<<ans<<endl;
	}
	return 0;
`}`