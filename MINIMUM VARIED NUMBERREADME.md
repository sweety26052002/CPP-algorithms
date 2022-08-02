# CPP-algorithms
t-shaped engineering
MINIMUM VARIED NUMBER
It is a codeforce problem
PROBLEM:
-----------------------------------------------------------------------------------------------------------------
/*Find the minimum number with the given sum of digits s such that all digits in it are distinct (i.e. all digits are unique).

For example, if s=20, then the answer is 389. This is the minimum number in which all digits are different and the sum of the digits is 20 (3+8+9=20).

For the given s print the required number.

Input
The first line contains an integer t (1≤t≤45) — the number of test cases.

Each test case is specified by a line that contains the only integer s (1≤s≤45).

Output
Print t integers — the answers to the given test cases.
Example
input
4
20
8
45
10
output
389
8
123456789
*/
-------------------------------------------------------------------------------------------------------------------------
EXPLAINATION
HERE the question given is
he will give a number so that u have to generate a number ,for that number the sum og digits  should be equal to the given number.
20 (3+8+9=20)
389
By seeing the example we can understand that there is no more number which is greater than 45 that generates a number which contains unique digits and sum of digits
is equal to the given number.
so if number <10 there is no problem cause sing unique digits
for 10 it is 19 given 
in the example--->1+9=10
for 11 we simply add +1 to the 1----->2+9=10.....so for 11 it is 29
12--->39
13---->49
.
.
.
17--->89
for 18 --->99(wrong)...cause 9 repeated for two times.
so make your 9 as 1+8
so for 18--->189(1+8+9)
19---->289
20--->389
Like this the numbers will change
---------------------------------------------------------------------------------------------------------------------
CODE:
#include<string>
#include<iostream>
using namespace std;
int main()
{
	int t;
	cin>>t;
	while(t)
	{
		int n;
		cin>>n;
		long long x;
		string s="";
		if(n<10)
		{
			cout<<n<<endl;
		
		}
		else
		{
		if(n>=10 && n<=17)
		{
			n=n-9;
            s=to_string(n);
            s=s+"9";
		}
		if(n>=18 && n<=24)
		{
			n=n-17;
            s=to_string(n);
            s=s+"89";
		}
		if(n>=25 && n<=30)
		{
			n=n-24;
            s=to_string(n);
            s=s+"789";
		}
		if(n>=31 && n<=35)
		{
			n=n-30;
            s=to_string(n);
            s=s+"6789";
		}
		if(n>=36 && n<=39)
		{
			n=n-35;
            s=to_string(n);
            s=s+"56789";
		}
		if(n>=40 && n<=42)
		{
			n=n-39;
            s=to_string(n);
            s=s+"456789";
		}
		if(n>=43 && n<=44)
		{
			n=n-42;
            s=to_string(n);
            s=s+"3456789";
		}
		if(n==45)
		{
			n=n-44;
			s=to_string(n);
			s=s+"23456789";
		}
		x=stol(s);
		cout<<x<<endl;
	}
 
t--;
	}
}
