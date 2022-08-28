```

Lecture 6: Operators and For Loop START HERE

```

# ##Lecture 6: Operators and For Loop

---

//============>>>>>>>>>>Lecture 6: Operators and For Loop
[Lecture 6: Operators and For Loop NOTES.pdf](https://github.com/karakib2k18/Cpp-Programming-Language-For-DSA/files/9434854/Lecture.6.Operators.and.For.Loop.NOTES.pdf)

---

###  Bitwise Operators

```cpp


/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;

int main() {
	int ror = 15 | 30;
	int rand = 15 & 30;
	int rnot = ~15;
	int rxor = 15 ^ 30;
	int rls = 15 << 2;
	int rrs = 15 >> 2;

	cout << ror << endl;
	cout << rand << endl;
	cout << rnot << endl;
	cout << rxor << endl;
	cout << rls << endl;
	cout << rrs << endl;
}
```

###  Increment Decrement Operators

```cpp


/*-------------------------------CODE------------------------*/
//-----------INCREMENT.CPP--------------
#include <iostream>
using namespace std;

int main() {
	int a = 10;
	a += 3;

	a*= 2;

	cout << a-- << endl;
	cout << --a << endl;
}

//--------PROCESS.CPP----------
#include <iostream>
using namespace std;

int main() {
	 int a = 2 * 3 + 4;
	 int b = (10 * 5) / 9;
	 cout << a << endl;
	 cout << b << endl;
}

```

###  For Loop

```cpp
//--------------print1toN.CPP--------------------
#include <iostream>
using namespace std;

int main() {
	int m,n;
	cout << "Enter m & n" << endl;
	cin >> m >> n;

	for(;m <= n; m++) {
		cout << m << endl;
	}
}

//-------------prime.cpp--------
#include <iostream>
using namespace std;

int main() {
	int n;
	cin >> n;

	bool divided = false;
	for (int d = 2;d < n; d++) {
		if (n % d == 0) {
			divided = true;
		}
	}

	if (divided) {
		cout << "Not prime" << endl;
	} else {
		cout << "Prime" << endl;
	}
}
```

###  Nth Fibonacci Number

```
Nth Fibonacci Number
 
Nth term of Fibonacci series F(n), where F(n) is a function, is calculated using the following formula -
    F(n) = F(n-1) + F(n-2), 
    Where, F(1) =  0, 
           F(2) = 1
Provided N you have to find out the Nth Fibonacci Number.
Input Format :
The first line of each test case contains a real number ‘N’.
Output Format :
For each test case, return its equivalent Fibonacci number.
Constraints:
1 <= N <= 10000     
Where ‘N’ represents the number for which we have to find its equivalent Fibonacci number.

Time Limit: 1 second
Sample Input 1:
6
Sample Output 1:
8
Explanation of Sample Input 1:
Now the number is ‘6’ so we have to find the “6th” Fibonacci number
So by using the property of the Fibonacci series i.e 

[ 1, 1, 2, 3, 5, 8]
So the “6th” element is “8” hence we get the output.
```

```cpp


/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;


int fiboa(int n){
    if(n==1 || n==2) return 1;
    return fiboa(n-1)+fiboa(n-2);
}

int main(){
    int n; cin>>n;
    cout<< fiboa(n);
}

```

###  Break and Continue

```cpp


/*-------------------------------CODE------------------------*/
//-----------------PRIME-----------------
#include <iostream>
using namespace std;

int main() {
	int n;
	cin >> n;
	int d = 2;
	bool divided = false;
	while (d < n) {
		if (n % d == 0) {
			divided = true;
			break;
		}
		d++;
	}
	if (divided) {
		cout << "Not prime" << endl;
	} else {
		cout << "Prime" << endl;
	}
}

//--------------BREAK------------------
#include <iostream>
using namespace std;

int main() {
	int n;
	cin >> n;

	int i = 1;
	while(i  <= n) {
		int j = 1;
		while (j <= n) {
			cout << j;
			j++;
			if (j > i) {
				break;
			}
		}
		cout << endl;
		i++;
	}
}

//------------FOR BREAK--------
#include <iostream>
using namespace std;

int main() {
	int n;
	cin >> n;
	bool divided = false;
	for (int d = 2; d < n; d++) {
		if (n % d == 0) {
			divided = true;
			break;
		}
	}
	if (divided) {
		cout << "Not Prime" << endl;
	} else {
		cout << "Prime" << endl;
	}
}

```

###  All Prime Numbers

```
All Prime Numbers
 
Given an integer N, print all the prime numbers that lie in the range 2 to N (both inclusive).
Print the prime numbers in different lines.
Input Format :
Integer N
Output Format :
Prime numbers in different lines
Constraints :
1 <= N <= 100
Sample Input 1:
9
Sample Output 1:
2
3
5
7
Sample Input 2:
20
Sample Output 2:
2
3
5
7
11
13
17
19
```

```cpp


/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;

int main(){

  int n; cin>>n;
  bool isprime;
    for(int i=2; i<=n; i++){
        isprime =false;
        for(int j=2; j<i; j++){
            if(i%j==0){
                isprime=true;
                break;
            }
        }
        if(!isprime){
            cout<< i<<endl;
        }
    }
}
```

###  Scope of Variables


```cpp


/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;

int main() {
	int i = 10;

	// not allowed int i = 22;
	cout << i << endl;

	if (i == 10) {
		int i = 23;
		cout << i << endl;
	}
	cout << i << endl;

	int k = 0;
	for (; k < 10; k++) {
		cout << k << endl;
	}
	cout << k << endl;
}

#include <iostream>
using namespace std;

int main() {
	int i = 1;
	while (i < 10) {
		int j = 1;
		while (j < i) {
			int k = 10;
			cout << j;
			j++;
		}
		cout <<k << endl;
		i++;
	}
}



#include <iostream>
using namespace std;

int main() {
	int k = 1;
	while (k < 100) {
		int k2 = 1002;
		cout << k2 << endl;
		k++;
	}
	cout << k2 << endl;

	int i = 10;
	cout << i << endl;

	if (i == 10) {
		int j = 12;
		cout << j << endl;
	} else {
		int j = 122;
		cout << j << endl;
	}
	// J is not available here 
	// cout << j << endl;
}

```

###  cin vs cin.get()

 

```cpp


/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;

int main() {
	char c;
	c = cin.get();
	int count = 0;
	while (c != '$') {
		count++;
		c = cin.get();
	}
	cout << count << endl;
}

```

###  Count Characters

```
Count Characters
 
Write a program to count and print the total number of characters (lowercase english alphabets only), digits (0 to 9) and white spaces (single space, tab i.e. '\t' and newline i.e. '\n') entered till '$'.
That is, input will be a stream of characters and you need to consider all the characters which are entered till '$'.
Print count of characters, count of digits and count of white spaces respectively (separated by space).
Input Format :
A stream of characters terminated by '$'
Output Format :
3 integers i.e. count_of_characters count_of_digits count_of_whitespaces (separated by space)
Sample Input :
abc def4 5$
Sample Output :
6 2 2
Sample Output Explanation :
Number of characters : 6 (a, b, c, d, e, f)
Number of digits : 2 (4, 5)
Number of white spaces : 2 (one space after abc and one newline after 4)
```

```cpp


/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;

int main() {
    char ch;
    ch = cin.get();
    int digits = 0, spaces = 0, characters = 0;
    while(ch != '$') {
        if(ch >= 'a' && ch <= 'z') {
            characters++;
        }
        else if(ch >= '0' && ch <= '9') {
            digits++;
        }
        else if(ch == ' ' || ch == '\t' || ch == '\n') {
            spaces++;
        }
        ch = cin.get();
    }
    cout << characters << " " << digits << " " << spaces;
}

```

###  Sum or Product

```
Sum or Product
 
Write a program that asks the user for a number N and a choice C. And then give them the possibility to choose between computing the sum and computing the product of all integers in the range 1 to N (both inclusive).
If C is equal to -
 1, then print the sum
 2, then print the product
 Any other number, then print '-1' (without the quotes)
Input format :
Line 1 : Integer N
Line 2 : Choice C
Output Format :
 Sum or product according to user's choice
Constraints :
1 <= N <= 12
Sample Input 1 :
10
1
Sample Output 1 :
55
Sample Input 2 :
10
2
Sample Output 2 :
3628800
Sample Input 3 :
10
4
Sample Output 3 :
-1
```

```cpp


/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;

int main() {
    int n,c,sum=0,pod=1;
    cin>>n>>c;
    if(c==1){
        for(int i=1; i<=n;++i){ 
            sum=sum+i;
        }
        cout<< sum <<endl;
    }else if(c==2){
                for(int i=1; i<=n;++i){ 
            pod=pod*i;
        }
        cout<< pod <<endl;
    }else{
        cout<< "-1"<<endl;
    }
    
}

```

###  Terms of AP

```
Terms of AP
 
Write a program to print first x terms of the series 3N + 2 which are not multiples of 4.
Input format :
Integer x
Output format :
Terms of series (separated by space)
Constraints :
1 <= x <= 1,000
Sample Input 1 :
10
Sample Output 1 :
5 11 14 17 23 26 29 35 38 41
Sample Input 2 :
4
Sample Output 2 :
5 11 14 17
```

```cpp


/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;

int main() {
    int n,x,y=0;
    cin>>n;
    for(int i=1; y<n; i++){
        x = 3*i+2;
        if(x%4!=0){
            y++;
        cout<<x<<" ";
        }
    }
}

```

###  Reverse of a number

```
Reverse of a number
 
Write a program to generate the reverse of a given number N. Print the corresponding reverse number.
Note : If a number has trailing zeros, then its reverse will not include them. For e.g., reverse of 10400 will be 401 instead of 00401.


Input format :
Integer N
Output format :
Corresponding reverse number
Constraints:
0 <= N < 10^8
Sample Input 1 :
1234
Sample Output 1 :
4321
Sample Input 2 :
1980
Sample Output 2 :
891
```

```cpp


/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;
const int N=1e9+10;

int main() {
    int n,rev_num=0; cin>>n;
    while(n!=0){
        rev_num = rev_num * 10 + n % 10;
        n=n/10;
    }
    cout<<rev_num;
}

```

###  Binary to decimal

```
Binary to decimal
 
Given a binary number as an integer N, convert it into decimal and print.
Input format :
An integer N in the Binary Format
Output format :
Corresponding Decimal number (as integer)
Constraints :
0 <= N <= 10^9
Sample Input 1 :
1100
Sample Output 1 :
12
Sample Input 2 :
111
Sample Output 2 :
7
```

```cpp


/*-------------------------------CODE------------------------*/
#include<iostream>
#include <cmath>
using namespace std;

int main() {
    int n,rem,sum=0,count=0; cin>>n;
    while(n!=0){
        rem = n%10;
        sum = sum + rem* pow(2,count);
        count++;
        n=n/10;
    }
        cout<< sum;
    
}

```

###  Decimal to Binary

```
Decimal to Binary
 
Given a decimal number (integer N), convert it into binary and print.
The binary number should be in the form of an integer.
Note: The given input number could be large, so the corresponding binary number can exceed the integer range. So you may want to take the answer as long for CPP and Java.


Note for C++ coders: Do not use the inbuilt implementation of "pow" function. The implementation of that function is done for 'double's and it may fail when used for 'int's, 'long's, or 'long long's. Implement your own "pow" function to work for non-float data types.


Input format :
Integer N
Output format :
Corresponding Binary number (long)
Constraints :
0 <= N <= 10^5
Sample Input 1 :
12
Sample Output 1 :
1100
Sample Input 2 :
7
Sample Output 2 :
111
```

```cpp


/*-------------------------------CODE------------------------*/
#include<iostream>
#include <cmath>
using namespace std;

int main() {
    // Write your code here
    int n; cin>>n;
    long binary=0, pow=1;
    while(n>0){
        int lastbit = n%2;
        // cout<<lastbit;
        binary = binary + lastbit*pow;
        pow= pow*10;
        n=n/2;
    }
    cout<<binary;
}

```

###  Square Root (Integral)

```
Square Root (Integral)
 
Given a number N, find its square root. You need to find and print only the integral part of square root of N.
For eg. if number given is 18, answer is 4.
Input format :
Integer N
Output Format :
Square root of N (integer part only)
Constraints :
0 <= N <= 10^8
Sample Input 1 :
10
Sample Output 1 :
3
Sample Input 2 :
4
Sample Output 2 :
2
```

```cpp


/*-------------------------------CODE------------------------*/
//A more optimised solution of this problem will be taught later

#include<iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    int output = 0;
    while(output * output <= n) {
        output = output + 1;
    }
    output = output - 1;
    cout << output;
}
```

### Check Number sequence

```
Check Number sequence
 
You are given S, a sequence of n integers i.e. S = s1, s2, ..., sn. Compute if it is possible to split S into two parts : s1, s2, ..., si and si+1, si+2, ….., sn (0 <= i <= n) in such a way that the first part is strictly decreasing while the second is strictly increasing one.
Note : We say that x is strictly larger than y when x > y.
So, a strictly increasing sequence can be 1 4 8. However, 1 4 4 is NOT a strictly increasing sequence.


That is, in the sequence if numbers are decreasing, they can start increasing at one point. And once the sequence of numbers starts increasing, they cannot decrease at any point further.
Sequence made up of only increasing numbers or only decreasing numbers is a valid sequence. So, in both the cases, print true.


You just need to print true/false. No need to split the sequence.
Input format :
Line 1 : Integer 'n'
Line 2 and Onwards : 'n' integers on 'n' lines(single integer on each line)
Output Format :
"true" or "false" (without quotes)
Constraints :
1 <= n <= 10^7
Sample Input 1 :
5
9
8
4
5
6
Sample Output 1 :
true
Sample Input 2 :
3
1
2
3
Sample Output 2 :
true
Sample Input 3 :
3
8
7
7
Sample Output 3 :
false
Explanation for Sample Format 3 :
8 7 7 is not strictly decreasing, so output is false.
Sample Input 4 :
6
8
7
6
5
8
2
Sample Output 4 :
false
Explanation for Sample Input 4 :
The series is :
8 7 6 5 8 2
It is strictly decreasing first (8 7 6 5). Then it's strictly increasing (5 8). But then it starts strictly decreasing again (8 2). Therefore, the output for this test case is 'false'
```

```cpp


/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;

int main() {
    int n;
    cin>>n;
    int current_term;
    cin>>current_term;
    bool isDecreasing = true,is_valid_sequence_yet=true;
    int i=2;// first term of sequence has already been taken
    while(i<=n){
        int next_term;
        cin>>next_term;
        if(is_valid_sequence_yet && isDecreasing && current_term>next_term){
            current_term=next_term;
            isDecreasing=true;
        }else if(is_valid_sequence_yet && current_term < next_term){
            current_term=next_term;
            isDecreasing = false;
        }else{
            is_valid_sequence_yet=false;
        }
        i++;
    }
    if(is_valid_sequence_yet){
        cout << "true" << endl;
    }else{
        cout << "false" <<endl;
    }
}
```

```

Lecture 6: Operators and For Loop END HERE

```