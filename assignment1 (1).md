



Assignment  (1)
Chapter Review
 1. What is a class?
A class combines data representation and functions  for manipulating that data into one neat package .it is a C++ vehicle for translating an abstraction to a user-defined type.
2. How does a class accomplish abstraction, encapsulation, and data hiding?
 A class design attempts to separate the public interface from the specifics of the implementation.The public interface represents the abstraction component of the design.
Gathering the implementation details together and separating them from the abstraction is called encapsulation.which is including data and functions in a class
Data hiding (putting data into the private section of a class) is an instance of encapsulation,and so is hiding functional details of an implementation in the private section
3. What is the relationship between an object and a class?
A class defines a type and how it can be used.
An object is a variable or another data which is created and used according to the class definition.
 Each new object you create contains storage for its own internal variables,the class members.But all objects of the same class share the same set of class methods,with just one copy of each method

4. In what way, aside from being functions, are class function members different from class data members?
Class Function members are public and class data members are private,
If you create several objects of a given class,each object comes with storage for its own set of data.But all the objects use the one set of member functions.



5. #include <iostream>
#include<cstring>
using namespace std;
 class BankAccount 
{
 private: 
string name;       
string accountnum;
 double balance;
 public: 
void BankAccount( string n,  char  num, double b );
void show ();
void deposit(double cash);
 void withdraw(double cash);
};


6. A class constructor is called when you create an object of that class.
While A class destructor is called when the object expires.


 7. #include <iostream>
#include"BankAccount.h"
#include <string>
using namespace std;
BankAccount:: BankAccount ()
{
	name = "unassigned";
	acctnum = "0000";        //initializing constructor;
	balance = 0;
}
void BankAccount :: show(){
	cout<<" depositor name : "<<name<<endl;
	cout<<" account number : "<<acctnum<<endl;
	cout<<" current balance : "<<balance<<endl;
} 
void BankAccount :: set_name (string n){
	name=n;
}
void BankAccount :: set_acctnum(string an){
	acctnum=an;
}
void BankAccount :: set_balance(int b){
	balance = b;
}
void BankAccount ::deposit(double cash){
	balance = balance + cash;
}
void BankAccount ::withdraw(double cash){
	balance = balance - cash;
}

8. A default constructor either has no arguments or has defaults for all the arguments. Having a default constructor enables you to declare objects without initializing them .It also allows you to declare arrays. 
9. #include <iostream>
using namespace std;
 class Stock 
{
 private:
 string company; 
long shares; 
double share_val; 
double total_val;
void set_tot(){ total_val = shares * share_val; }
 public:
 Stock();            
string & co, long n, double pr); 
Stock() {}         
void buy(long num, double price);
 void sell(long num, double price); 
void update(double price);
 void show() const; const Stock & topval(const Stock & s) const; 
int numshares() const { return shares; } 
double shareval() const { return share_val; }
 double totalval() const { return total_val; }
 const string & co_name() const { return company; } }
10. this  is available to class methods.It points to the object used to invoke the method.this is the address of the object
and *this represents the object itself.
