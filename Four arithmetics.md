# HealerHelen
//Zhao Ziyin，20160303，four arithmetics

#include<iostream>
#include<time.h>
#include<string>
using namespace std;
#define N 30
#define random(x) (rand()%x)

void main()
{
   while (true)
  {
	   cout << "-----------Choose the form of formulas 1 or 2:--------------" << endl;
	   cout << "              Ⅰ. Integers(like  35 + 64 = )                " << endl;  
	   cout << "              Ⅱ. Proper fraction(like  5/6 × 7/10 = )     " << endl;
	   int num,i;
	   int sign_num;
	   int change;
	   cin >> num;

	   if (num == 1)
	   {
		   srand((int)time(0));
		   cout << endl;
		   cout << "-----There are " << N << " arithmetic problems:-----" << endl;
		  
		   for (i = 1; i <=N; i++)
		   {
			   int one, two;
			   /*srand((int)time(0));*/
			   one = rand() % (99 + 1) + 1;
			   two = rand() % (99 + 1) + 1;

			   /*srand((int)time(0));*/
			   sign_num = (rand() % (99 + 1) + 1) % 4;
			   switch (sign_num)
			   {
			   case(0) :
				   cout <<i<<".  ";
				   cout << one << " + " << two << " = " << endl;
				   break;
			   case(1) :
				   if (one < two)
				   {
					   change = one;
					   one = two;
					   two = change;
				   }
				   cout << i << ".  ";
				   cout << one << " - " << two << " = " << endl;
				   break;
			   case(2) :
				   cout << i << ".  ";
				   cout << one << " × " << two << " = " << endl;
				   break;
			   case(3) :
				   if (one < two)
				   {
					   change = one;
					   one = two;
					   two = change;
				   }
				   cout << i << ".  ";
				   cout << one << " ÷ " << two << " = " << endl;
				   break;
			   }
		   }
	   }

	   else if (num == 2)
	   {
		   string sign;
		   srand((int)time(0));
		   cout << endl;
		   cout << "-----There are " << N << " proper fraction arithmetic problems:-----" << endl;

		   for (i = 1; i <= N; i++)
		   {
			   sign_num = (rand() % (99 + 1) + 1) % 4;
			   switch (sign_num)
			   {
			   case(0) :
				   sign = '+'; break;
			   case(1) :
				   sign = '-'; break;
			   case(2) :
				   sign = '*'; break;
			   case(3) :
				   sign = '/'; break;
			   }

			   int one, two,three,four;
			   /*srand((int)time(0));*/
			   one = rand() % (99 + 1) + 1;
			   two = rand() % (99 + 1) + 1;
			   three = rand() % (99 + 1) + 1;
			   four = rand() % (99 + 1) + 1;
			   if (one > two)
			   {
				   change = one;
				   one = two;
				   two = change;
			   }
			   if (three > four)
			   {
				   change = three;
				   three = four;
				   four = change;
			   }

			   int oper_num;
			   oper_num = (rand() % (99 + 1) + 1) % 3;
			   switch (oper_num)
			   {
			   case(0) :
				   cout << i << ".  ";
				   cout << one << "/" << two << " " << sign << " " << three << "/" << four << " = " << endl;
				   break;
			   case(1) :
				   cout << i << ".  ";
				   cout << one << "/" << two << " " << sign << " " <<four<< " = " << endl;
				   break;
			   case(2) :
				   cout << i << ".  ";
				   cout << one << " " << sign << " " << three << "/" << four << " = " << endl;
				   break;
			   }

			  
		 }
	 }
 }

}



