[](https://www.lanqiao.cn/courses/21965/learning/?id=1149557&compatibility=false)

#include<bits/stdc++.h>
using namespace std;
int main()
{
  //测试用例的数量
  int t;
  cin>>t;
  while(t--)
  {
    //输入房间数和区间k
  int n;
  int k;
  cin>>n>>k;
  //一个数组来存放每个房间的颜色
  int a[n];
  //输入每个房间的颜色
  for(int i=0;i<n;i++)
  {
    cin>>a[i];
  }
  //假设需要最大的天数为1e4
  int res=1e4;
  //暴力枚举,所有的房间要被涂成同一颜色,有60种可能
   for(int i=1;i<=60;i++)
   {
     //初始化涂漆天数为 0天,如果颜色不一致则++
    int ans=0;
     for(int j=0;j<n;j++)
     {
     if(a[j]!=i)
       {
     ans++;
     j=j+(k-1);
       } 
      }
      res=min(ans,res);
   }
   cout<<res<<endl;
  }
  return 0;
}