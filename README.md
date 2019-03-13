
		
		
		
#include "pch.h"
#include <iostream>
#include"time.h"
using namespace std;
int main()
{
	int a[40];
	float answers[10];
	float correctanswers[10];
	int time1, time2;
	srand((unsigned)time(0));
	time1 = time(0);
	char sign[30];
	for (int i = 0; i < 40; i++) {
		a[i] = rand() % 101;
	}
	int q, p;
	q = 0;
	p = 0;
	for (int j = 0; j < 40; j = j + 4) {
		float b, c;
		int k = rand() % 4;
		char C;
		if (k == 0)
		{
			C = '+'; sign[j / 4] = C;
		}
		else if (k == 1)
		{
			C = '-'; sign[j / 4 * 3] = C;
		}
		else if (k == 2)
		{
			C = '*'; sign[j / 4 * 3] = C;
		}
		else if (k == 3)
		{
			C = '/'; sign[j / 4 * 3] = C;
		}
		int x = rand() % 4;
		char D;
		if (x == 0)
		{
			D = '+'; sign[j / 4 * 3 + 1] = D;
		}
		else if (x == 1)
		{
			D = '-'; sign[j / 4 * 3 + 1] = D;
		}
		else if (x == 2)
		{
			D = '*'; sign[j / 4 * 3 + 1] = D;
		}
		else if (x == 3)
		{
			D = '/'; sign[j / 4 * 3 + 1] = D;
		}
		int y = rand() % 4;
		char E;
		if (y == 0)
		{
			E = '+'; sign[j / 4 * 3 + 2] = E;
		}
		else if (y == 1)
		{
			E = '-'; sign[j / 4 * 3 + 2] = E;
		}
		else if (y == 2)
		{
			E = '*'; sign[j / 4 * 3 + 2] = E;
		}
		else if (y == 3)
		{
			E = '/'; sign[j / 4 * 3 + 2] = E;
		}
		if (k == 0) {
			if (x == 0) {
				if (y == 0)b = a[j] + a[j + 1] + a[j + 2] + a[j + 3];
				else if (y == 1) b = a[j] + a[j + 1] + a[j + 2] - a[j + 3];
				else if (y == 2)b = a[j] + a[j + 1] + a[j + 2] * a[j + 3];
				else b = a[j] + a[j + 1] + a[j + 2] / a[j + 3];
				correctanswers[j / 4] = b;
			}
			else if (x == 1) {
				if (y == 0) b = a[j] + a[j + 1] - a[j + 2] + a[j + 3];
				else if (y == 1) b = a[j] + a[j + 1] - a[j + 2] - a[j + 3];
				else if (y == 2)b = a[j] + a[j + 1] - a[j + 2] * a[j + 3];
				else b = a[j] + a[j + 1] - a[j + 2] / a[j + 3];
				correctanswers[j / 4] = b;
			}
			else if (x == 2) {
				if (y == 0) b = a[j] + a[j + 1] * a[j + 2] + a[j + 3];
				else if (y == 1) b = a[j] + a[j + 1] * a[j + 2] - a[j + 3];
				else if (y == 2)b = a[j] + a[j + 1] * a[j + 2] * a[j + 3];
				else b = a[j] + a[j + 1] * a[j + 2] / a[j + 3];
				correctanswers[j / 4] = b;
			}
			else {
				if (y == 0) b = a[j] + a[j + 1] / a[j + 2] + a[j + 3];
				else if (y == 1) b = a[j] + a[j + 1] / a[j + 2] - a[j + 3];
				else if (y == 2)b = a[j] + a[j + 1] / a[j + 2] * a[j + 3];
				else b = a[j] + a[j + 1] / a[j + 2] / a[j + 3];
				correctanswers[j / 4] = b;
			}
		}
		else if (k == 1) {
			if (x == 0) {
				if (y == 0)b = a[j] - a[j + 1] + a[j + 2] + a[j + 3];
				else if (y == 1) b = a[j] - a[j + 1] + a[j + 2] - a[j + 3];
				else if (y == 2)b = a[j] - a[j + 1] + a[j + 2] * a[j + 3];
				else b = a[j] - a[j + 1] + a[j + 2] / a[j + 3]; correctanswers[j / 4] = b;
			}
			else if (x == 1) {
				if (y == 0) b = a[j] - a[j + 1] - a[j + 2] + a[j + 3];
				else if (y == 1) b = a[j] - a[j + 1] - a[j + 2] - a[j + 3];
				else if (y == 2)b = a[j] - a[j + 1] - a[j + 2] * a[j + 3];
				else b = a[j] - a[j + 1] - a[j + 2] / a[j + 3]; correctanswers[j / 4] = b;
			}
			else if (x == 2) {
				if (y == 0) b = a[j] - a[j + 1] * a[j + 2] + a[j + 3];
				else if (y == 1) b = a[j] - a[j + 1] * a[j + 2] - a[j + 3];
				else if (y == 2)b = a[j] - a[j + 1] * a[j + 2] * a[j + 3];
				else b = a[j] - a[j + 1] * a[j + 2] / a[j + 3]; correctanswers[j / 4] = b;
			}
			else {
				if (y == 0) b = a[j] - a[j + 1] / a[j + 2] + a[j + 3];
				else if (y == 1) b = a[j] - a[j + 1] / a[j + 2] - a[j + 3];
				else if (y == 2)b = a[j] - a[j + 1] / a[j + 2] * a[j + 3];
				else b = a[j] - a[j + 1] / a[j + 2] / a[j + 3]; correctanswers[j / 4] = b;
			}
		}
		else if (k == 2) {
			if (x == 0) {
				if (y == 0)b = a[j] * a[j + 1] + a[j + 2] + a[j + 3];
				else if (y == 1) b = a[j] * a[j + 1] + a[j + 2] - a[j + 3];
				else if (y == 2)b = a[j] * a[j + 1] + a[j + 2] * a[j + 3];
				else b = a[j] * a[j + 1] + a[j + 2] / a[j + 3]; correctanswers[j / 4] = b;
			}
			else if (x == 1) {
				if (y == 0) b = a[j] * a[j + 1] - a[j + 2] + a[j + 3];
				else if (y == 1) b = a[j] * a[j + 1] - a[j + 2] - a[j + 3];
				else if (y == 2)b = a[j] * a[j + 1] - a[j + 2] * a[j + 3];
				else b = a[j] * a[j + 1] - a[j + 2] / a[j + 3]; correctanswers[j / 4] = b;
			}
			else if (x == 2) {
				if (y == 0) b = a[j] * a[j + 1] * a[j + 2] + a[j + 3];
				else if (y == 1) b = a[j] * a[j + 1] * a[j + 2] - a[j + 3];
				else if (y == 2)b = a[j] * a[j + 1] * a[j + 2] * a[j + 3];
				else b = a[j] * a[j + 1] * a[j + 2] / a[j + 3]; correctanswers[j / 4] = b;
			}
			else {
				if (y == 0) b = a[j] * a[j + 1] / a[j + 2] + a[j + 3];
				else if (y == 1) b = a[j] * a[j + 1] / a[j + 2] - a[j + 3];
				else if (y == 2)b = a[j] * a[j + 1] / a[j + 2] * a[j + 3];
				else b = a[j] * a[j + 1] / a[j + 2] / a[j + 3]; correctanswers[j / 4] = b;
			}
		}
		else {
			if (x == 0) {
				if (y == 0)b = a[j] / a[j + 1] + a[j + 2] + a[j + 3];
				else if (y == 1) b = a[j] / a[j + 1] + a[j + 2] - a[j + 3];
				else if (y == 2)b = a[j] / a[j + 1] + a[j + 2] * a[j + 3];
				else b = a[j] / a[j + 1] + a[j + 2] / a[j + 3]; correctanswers[j / 4] = b;
			}
			else if (x == 1) {
				if (y == 0) b = a[j] / a[j + 1] - a[j + 2] + a[j + 3];
				else if (y == 1) b = a[j] / a[j + 1] - a[j + 2] - a[j + 3];
				else if (y == 2)b = a[j] / a[j + 1] - a[j + 2] * a[j + 3];
				else b = a[j] / a[j + 1] - a[j + 2] / a[j + 3]; correctanswers[j / 4] = b;
			}
			else if (x == 2) {
				if (y == 0) b = a[j] / a[j + 1] * a[j + 2] + a[j + 3];
				else if (y == 1) b = a[j] / a[j + 1] * a[j + 2] - a[j + 3];
				else if (y == 2)b = a[j] / a[j + 1] * a[j + 2] * a[j + 3];
				else b = a[j] / a[j + 1] * a[j + 2] / a[j + 3]; correctanswers[j / 4] = b;
			}
			else {
				if (y == 0) b = a[j] / a[j + 1] / a[j + 2] + a[j + 3];
				else if (y == 1) b = a[j] / a[j + 1] / a[j + 2] - a[j + 3];
				else if (y == 2)b = a[j] / a[j + 1] / a[j + 2] * a[j + 3];
				else b = a[j] / a[j + 1] / a[j + 2] / a[j + 3]; correctanswers[j / 4] = b;
			}
		}
		cout << a[j] << C << a[j + 1] << D << a[j + 2] << E << a[j + 3] << "=";
		cin >> c;
		answers[j / 4] = c;
		if (c == b) q++;
		else p++;
	}
	time2 = time(0);
	int time0 = time2 - time1;
	cout << "time used:" << time0 << "seconds" << endl;
	cout << "correct:" << q << endl;
	cout << "errors:" << p << ',' << "they are:" << endl;

	time2 = time(0);
	for (int z = 0; z <= 9; z = z + 1) {
		if (answers[z] != correctanswers[z]) {

			cout << a[z * 4] << sign[z * 3] << a[z * 4 + 1] << sign[z * 3 + 1] << a[z * 4 + 2] << sign[z * 3 + 2] << a[z * 4] << '=' << correctanswers[z] << endl;
		}
	}
}

