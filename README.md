#include<iostream>
#include<math.h>
using namespace std;
class Vector
{
//创建私有变量
private:
	int x;
	int y;

public:

	//构造函数
	Vector(int x,int y):x(x),y(y)
	{
		
	}

	//将两个向量相加
	Vector add(const Vector& v)
	{
		int plusx = x + v.x;
		int plusy = y + v.y;
		return Vector (plusx,plusy);
	}
	
	//输出此向量
	void print()
	{
		cout << "("<< x << "," << y << ")"<<endl;
	}

	//求向量模长并打印输出
	void dir(int x, int y,int x1,int y1)
	{
		double l = sqrt( (x+x1)* (x+x1) + (y+y1) * (y+y1) );
		cout <<"向量的模长为"<< l << endl;
	}
};



int main()
{	
	Vector a(3 , 0);
	Vector b(0 , 4);
	
	cout << "向量a为";
	a.print();
	
	cout << "向量b为";
	b.print();

	Vector plus =  a.add(b);
	cout << "两个向量相加等于：";
	plus.print();

	a.dir(3, 0, 0, 4);
	
	return 0;
}
