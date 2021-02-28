# Roman-Dubil KN-102
//Створити клас – коло. У закритій частині описати поля: координати центру та радіус. Визначити конструктор, деструктор, зміни значень полів і отримання їхніх значень, виведення //полів класу, обчислення площі та довжини кола. Функції зміни значень полів класу повинні перевіряти коректність параметрів, що задаються.
#include <iostream>

#include <cmath>
#define PI 3.14


using namespace std;



class Cirle
{

private:

	int x;

	int y;

	int radius;



public:

	Cirle(int a, int b, int c) { x = a; y = b; radius = c; }

	~Cirle() {}



	int GetX() { return x; }

	int GetY() { return y; }

	int GetRadius() { return radius; }


	void SetX(int a) { x = a; }

	void SetY(int b) { y = b; }

	void SetRadius(int c) { radius = c; }
	/////////////////////////////////////


	double square(Cirle& obj);

	double longOfcirle(Cirle& obj);

};



double Cirle::square(Cirle& obj)
{
	return (PI * pow(radius, 2));

}

double Cirle::longOfcirle(Cirle& obj)
{
	return (2 * PI * radius);

}
///////////////////////////////////////////////////////////


int main()

{

	Cirle obj(1, 2, 3);


	cout << obj.GetX() << endl;
	cout << obj.GetY() << endl;
	cout << obj.GetRadius() << endl;


	cout << obj.square(obj) << endl;
	cout << obj.longOfcirle(obj) << endl;


	obj.SetX(6);
	obj.SetY(5);
	obj.SetRadius(5);

	cout << obj.GetX() << endl;
	cout << obj.GetY() << endl;
	cout << obj.GetRadius() << endl;


	cout << obj.square(obj) << endl;
	cout << obj.longOfcirle(obj) << endl;


	return 0;

}
