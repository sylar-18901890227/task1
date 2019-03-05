# task1
#include "pch.h"
#include <iostream>
#include"time.h"
using namespace std;
int main()
{
	int a, b, c, d, n;
	cin >> n;
	srand(time(0));
	
		a = rand() % 101;
		b = rand() % 101;
		c = rand() % 101;
		d = rand() % 101;
		cout << a << '+' << b << '-' << c << '/' << d << endl;
		cout << a + b - c / d << endl;
		if (n ==1) {
			return 0;
		}
		a = rand() % 101;
		b = rand() % 101;
		c = rand() % 101;
		d = rand() % 101;
		cout << d << '-' << b << '*' << a << endl;
		cout << d - b * a << endl;
		if (n == 2) {
			return 0;
		}
		a = rand() % 101;
		b = rand() % 101;
		c = rand() % 101;
		d = rand() % 101;
		cout << a << '-' << b << '-' << c << '-' << d << endl;
		cout << a - b - c - d<<endl;
		if (n == 3) {
			return 0;
		}
		a = rand() % 101;
		b = rand() % 101;
		c = rand() % 101;
		d = rand() % 101;
		cout << a << '+' << b << '+' << c << '+' << d << endl;
		cout << a + b + c + d << endl;
		cout << 1750223<< "何韫惟" << endl;
	
}
