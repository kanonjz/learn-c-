# 容器
### vector
vector相当于动态数组，无需提前声明大小，支持随机访问，可以通过下标进行访问。
```
#include <iostream>
#include <vector>

using namespace std;

int main(){
	//声明vector，无需指定大小 
	vector<int> v;
	//在末尾插入 
	v.push_back(3);
	v.push_back(4);
	v.push_back(5);
	v.push_back(6);
	v.push_back(7);
	//利用迭代器遍历元素 
	for(vector<int>::iterator i=v.begin();i!=v.end();i++){
		cout<<" "<<*i;
	}
	cout<<"\n";
	//删除尾元素 
	v.pop_back();
	//判断是否为空 
	cout<<v.empty()<<endl;
	//支持下标随机访问 
	cout<<v[0]<<v[1]; 
}
```
