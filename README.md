# learnPointer
#include<string>
#include<iostream>
using namespace std;
class usingcopyconstructor
{
private:
	int eutainteger;
	int *p = new int[3];
public:
	
	usingcopyconstructor();
	usingcopyconstructor(const usingcopyconstructor& object);//remember the syntax for using the copy constructor, you should use const and & (passing by reference, there is no copy of the value of the object, that is the reason why you pass by reference
	void print()const;
	~usingcopyconstructor();
};
//implementation of the class
usingcopyconstructor::usingcopyconstructor()
{
	eutainteger = 9;
	p[0] = 0;
	p[1] = 1;
	p[2] = 2;
	
}
usingcopyconstructor::usingcopyconstructor(const usingcopyconstructor& object)
{
	eutainteger=object.eutainteger;
	p[0] = object.p[0];
	p[1] = object.p[1];
	p[2] = object.p[2];
	

}
void usingcopyconstructor::print()const
{
	cout << eutainteger << endl;
	cout << p[0] << endl;
	cout << p[1] << endl;
	cout << p[2] << endl;
}
usingcopyconstructor::~usingcopyconstructor()
{
	delete[]p;
	p[0], p[1], p[2] = NULL;
}
//*************************************************************************************************
//this class section is for the third program
//class oiee
//{
//public:
//	int ullu;
//
//};
//**********************************************************************************************
int main()
{
	/*int a = 30;
	int *p;
	p = &a;
	*p = 35;
	cout << *p;
	return 0;*/
	//***********************************************************************************
	//int * z;
	//z = NULL;
	//*z = 35;//here you are trying to deference a NULL pointer.. you need to unederstand that dereferencing occurs only with the help of address location
	//cout << *z << z;
	//return 0;
	//************************************************************************************
	/*struct name {
		int a;
		char an;
		string ant;
	};
	name point,point1;
	name* pointer;
	point1.a = 6;
	pointer = &point;
	(*pointer).a = 5;
	cout << (pointer->a);
	oiee oieekoobject;
	oiee* oieobjectlaipointgarnepointer;
	oieobjectlaipointgarnepointer = &oieekoobject;
	oieobjectlaipointgarnepointer->ullu = 3;*/
	////*****************************************************************************************
	//int *p;//declaring a poointer, why?? -- i might need to store the address of some variable and change it later on
	//// we introduce new operator to allocate memory, here we dont need to use any assignment & operator
	//p = new int;//lets start with single variable memory allocation
	//*p = 35;
	//
	//cout << *p;//if you lool at first program you tried(and things I learned section), you can see that unilitialized local variable problem can be removed with the help of new operator

	//return 0;
	//**************************************************************************************************
	
	//int d;
	//cout << "no.of names you want to store";
	//cin >> d;
	//string* name;// name is a pointer
	//name = new string[d];// we are creating an array of d variables and the address of the base of the this array i stored in name
	//for (int i = 0; i < d; i++)
	//{
	//	cin >> name[i];
	//}
	//name[d - 1] = "changed";
	//*name = "try";
	//for (int i = 0; i < d; i++)
	//{
	//	cout << name[i];
	//}
	//delete []name;
	//
	//return 0;
	//*******************************************************************************************
	//copy constructor
	//making an object of class usingcopyconstructor
	usingcopyconstructor eutaobject;
	usingcopyconstructor arkoobject(eutaobject);
	arkoobject.print();
	
	
	return 0;

}

//things I learned:
/* unilitializzed local variable means you are trying to dereference a pointer without initializing its location,
thus it is important to provide a location for a pointer before you dereference it*/
