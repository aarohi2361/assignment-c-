#include<iostream>
#include<string.h>
using namespace std;



int main() {


	int n;
	cout << "enter n number of arguments you want to input" << "\n";
	cin >> n;
	cout<<"please enter numbers one by one"<<"\n";
	int min = 2147483647;
	for (int i = 0; i < n; i++)
	{
		int isNumber = 1;
		while(isNumber)
		{
		string something;
		cin >> something;
		int will;
		for (int i = 0; i < something.length(); i++)
		{
			if (isdigit(something[i]) == false)
			{
				will = 0;
				break;
			} else {
				will = 1;
			}


		}
		if (will == 1)
		{
			int num = stoi(something) ;
			if(num<min)
			{
				min = num;
			}
			isNumber = 0;
		}else{
			cout<<"pls!! enter a prober number...."<<"\n";
		}


		}

	}

      cout<<"The smallest number is : " << min ;

	return 0;
}