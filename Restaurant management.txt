#include"stdafx.h"
#include<iostream>
using namespace std;
double bill[6]={0,0,0,0,0,0};
double drink(double x)
{
	double l;
	cout<<"\t|| Enter total drinks                     ||:\t ";
	cin>>x;
	l=x*6.95;
	bill[0]+=l;
	cout<<"\t|| total entred drinks are         "<<x<<"||"<<endl;
	return 0;
}
double Burger(double x)
{
	double l;
	cout<<"\t|| Enter total Burgers                    ||:\t ";
	cin>>x;
	l=x*5.75;
	bill[1]+=l;
	cout<<"\t|| total entred burgers are        "<<x<<"||"<<endl;
	return 0;
}
double sandwich(double x)
{
	double l;
	cout<<"\t||Enter total sandwiches                  ||:\t ";
	cin>>x;
	l=x*7.25;
	bill[2]+=l;
	cout<<"\t|| total entred sandwiches are     "<<x<<"||"<<endl;
	return 0;
}
double nuggets(double x)
{
	double l;
	cout<<"\t||       Enter total nuggets              ||:\t ";
	cin>>x;
	l=x*8.95;
	bill[3]+=l;
	cout<<"\t|| total entred nuggets are        "<<x<<"||"<<endl;
	return 0;
}
double chips(double x)
{
	double l;
	cout<<"\t||   Enter total chips                    ||:\t ";
	cin>>x;
	l=x*4.95;
	bill[4]+=l;
	cout<<"\t||   total entred  chips are       "<<x<<"||"<<endl;
	return 0;
}
double friedrice(double x)
{
	double l;
	cout<<"\t||      Enter total fried rice            ||:\t ";
	cin>>x;
	l=x*12.95;
	bill[5]+=l;
	cout<<"\t||  total entred  fried rice  are  "<<x<<"||"<<endl;
	return 0;
}
int main()
{
	int m;
	 cout<<"\t||:::::::::Welcome to Diva resturant::::::::::||"<<endl; 
	 cout<<"\t||:::::::::::::::::::MENU:::::::::::::::::::||"<<endl;
     cout<<"\t|| Item[0] drinks   \t\t$6.95 ||"<<endl;
     cout<<"\t|| Item[1] Burger  	\t$5.75 ||"<<endl;
	 cout<<"\t|| Item[2] Sandwich	\t$7.25 ||"<<endl;
	 cout<<"\t|| Item[3] Nuggets  \t\t$8.95 ||"<<endl;
	 cout<<"\t|| Item[4] chips    \t\t$4.95 ||"<<endl;
	 cout<<"\t|| item[5] fried rice\t\t$12.35||"<<endl;
	 cout<<"\t||     [7] to end                     ||"<<endl;
	const char *item[7]={"Drink","Burger","Sandwich","Nuggets","Chips","Renter","end"};
	double food[6]={6.95,5.75,7.25,8.95,4.95,12.35};
	int count=0;
	while (m!=7)
	{
	cout<<"\t||     Enter your Order               ||: ";
	cin>>m;
	switch (m)
	{
	case 0:
	   {
		int x=0;
		cout<<"\t||1 "<<item[0]<<" With price "<<food[0]<<"||"<<endl;
		drink(x);
		count++;
		break;
	   }
	case 1:
	   {
		int x=0;
		cout<<"\t||1 "<<item[1]<<" with price "<<food[1]<<"||"<<endl;
		Burger(x);
		count++;
		break;
	   }
	case 2:
		{
		int x=0;
		cout<<"\t||1 "<<item[2]<<" with price "<<food[2]<<"||"<<endl;
		sandwich(x);
		count++;
		break;
		}
	case 3:
		{
		int x=0;
		cout<<"\t||1 "<<item[3]<<" with price "<<food[3]<<"||"<<endl;
		nuggets(x);
		count++;
		break;
		}
	case 4:
		{
		int x=0;
		cout<<"\t||1 "<<item[4]<<" with price "<<food[4]<<"||"<<endl;
		chips(x);
		count++;
		break;
		}
	case 5:
		{
		int x=0;
		cout<<"\t||1 "<<item[5]<<" with price "<<food[5]<<"||"<<endl;
		friedrice(x);
		count++;
		break;
		}
	default: cout<<"||Please enter a vaild value!!!||"<<endl;
		if (count=4){
			break;
		}
	}
	}
	
	cout<<"\t|| Total bill is                 ||"<<endl;
	cout<<"\t|| Total items    "<<count<<"    ||"<<endl;
	for (int i=0;i<6;i++)
	{
    cout<<"\t||"<<bill[i]<<"$  for "<<item[i]<<"     ||"<<endl;
	}
	double d=0;
	for (int i=0;i<7;i++)
	{
		d+=bill[i];
	}
	cout<<"\t||  "<<d<<"$ Total bill              ||"<<endl;
	system("pause");
	return 0;
}

