## delete和delete[ ]区别
例子：
```
class T {
	public:
	  T() { cout << "constructor" << endl; }
	  ~T() { cout << "destructor" << endl; }
};
 
int main()
{	
	T* p1 = new T[3];
	delete p1;
	
	T* p2 = new T[3];
	delete[] p2;
  
  T* p3 = new T;
	delete p3;
}
```
输出结果：
```
constructor
constructor
constructor
destructor

constructor
constructor
constructor
destructor
destructor
destructor

constructor
destructor
```
结论：
1. delete用来释放new分配的单个对象指针指向的内存
2. delete[]用来释放new分配的对象数组指针指向的内存

另外：
对于基本类型，使用`delete`或`delete[]`都是可以的。  
因为在分配基本类型内存时，内存大小已经确定，系统可以记忆并且进行管理，在析构时，系统并不会调用析构函数。
```
int* a = new int[4];
delete a; //delete[] a 也是可以的
```

