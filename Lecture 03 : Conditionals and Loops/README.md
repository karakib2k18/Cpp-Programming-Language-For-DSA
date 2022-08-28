```

Lecture 3 : Conditionals and Loops START HERE

```

# ##Lecture 3 : Conditionals and Loops

---

//============>>>>>>>>>> Lecture 3 : Conditionals and Loops
[Lecture 3 : Conditionals and Loops NOTES.pdf](https://github.com/karakib2k18/Cpp-Programming-Language-For-DSA/files/9434598/Lecture.3.Conditionals.and.Loops.NOTES.pdf)

---

###  Conditionals

```cpp
#include <iostream>
using namespace std;

int main() {
	int a, b;
	cout << "Enter two numbers" << endl;

	cin >> a >> b;

	if (a == b) {
		cout << "Hey these are equal" << endl;
	} else if (a < b) {
		cout << "a is smaller" << endl;
	} else {
		cout << "a is greater" << endl;
	}
	

	cout << "Enter the number" << endl;
	cin >> n;

	if (n % 2 == 0) {
		cout << "Even" << endl;
	} else {
		cout << "Odd" << endl;
	}


	/*
	if (a == b) {
		cout << "Hey these are equal" << endl;
	} else {
		if (a < b) {
			cout << "a is smaller" << endl;
		} else {
			cout << "a is greater" << endl;
		}
	}
  */
	/*
	if (a == b) {
		cout << "Hey these are equal" << endl;
	}


	 if (a == b) {
		cout << "Hey these are equal" << endl;
	} else {
		cout << "Not equal" << endl;
	}
	*/

	// Single line comment
}

```

###  Check Case

```
Check Case
 
Write a program that takes a character as input and prints either 1, 0 or -1 according to the following rules.
1, if the character is an uppercase alphabet (A - Z)
0, if the character is a lowercase alphabet (a - z)
-1, if the character is not an alphabet
Input format :
Single Character
Output format :
1 or 0 or -1
Constraints :
Input can be any character
Sample Input 1 :
v
Sample Output 1 :
0
Sample Input 2 :
V
Sample Output 2 :
1
Sample Input 3 :
#
Sample Output 3 :
-1
```

```cpp
#include<iostream>
using namespace std;

int main() {
	char c;
    cin>>c;
    if(c >= 'a' && c <= 'z')
    {
       cout<<"0"<<endl;
    }
    else if(c >= 'A' && c <= 'Z')
    {
       cout<<"1"<<endl;
    }
    else
    {
       cout<<"-1"<<endl;
    }
	
}
```

###  Understanding While Loop

```cpp
#include <iostream>
using namespace std;

int main() {
	int n;
	cout << "Enter n" << endl;

	cin >> n;

	int i = 1;
	while (i <= n) {
		cout << i << endl;
		i = i + 1;
	}
}
```

###  More on While Loop

```cpp
#include <iostream>
using namespace std;

int main() {
	int n;
	cout << "Enter n" << endl;
	cin >> n;

	int d = 2;
	bool divided = false;
	while (d < n) {
		if (n % d == 0) {
			cout << "Not Prime" << endl;
			divided = true;
		}
		d = d + 1;
	}
	if (!divided) {
		cout << "Prime" << endl;
	}
}
```

###  Sum of Even Numbers till N

```
Sum of Even Numbers till N
 
Given a number N, print sum of all even numbers from 1 to N.
Input Format :
Integer N
Output Format :
Required Sum 
Sample Input 1 :
 6
Sample Output 1 :
12
```

```cpp
/*-------------------------------CODE------------------------*/

#include<iostream>
using namespace std;


int main(){
	int n;
	double sum=0;
	cin>>n;
	for(int i=2;i<=n; i=i+2){
		sum = sum + i;
	}
	cout<< sum <<endl;  
}
```

###  Fahrenheit to Celsius Table

```
Fahrenheit to Celsius Table
 
Given three values - Start Fahrenheit Value (S), End Fahrenheit value (E) and Step Size (W), you need to convert all Fahrenheit values from Start to End at the gap of W, into their corresponding Celsius values and print the table.
Input Format :
3 integers - S, E and W respectively 
Output Format :
Fahrenheit to Celsius conversion table. One line for every Fahrenheit and corresponding Celsius value. The Fahrenheit value and its corresponding Celsius value should be separate by single space.
Constraints :
0 <= S <= 90
S <= E <=  900
0 <= W <= 80 
Sample Input 1:
0 
100 
20
Sample Output 1:
0   -17
20  -6
40  4
60  15
80  26
100 37
Sample Input 2:
20
119
13
Sample Output 2:
20  -6
33  0 
46  7
59  15
72  22
85  29
98  36
111 43
Explanation For Input 2:
Start calculating the Celsius values for each Fahrenheit Value which starts from 20. So starting from 20, we need to compute its corresponding Celsius value which computes to -6. We print this information as <Fahrenheit Value> <a single space> <Celsius Value> on each line. Now add 13 to Fahrenheit Value at each step until you reach 119 in this case. You may or may not exactly land on the end value depending on the steps you are taking.
```

```cpp
/*-------------------------------CODE------------------------*/
// Fahrenheit to Celsius Table
// https://classroom.codingninjas.com/app/classroom/me/14886/content/276725/offering/3796228/problem/966

#include<iostream>
using namespace std;


int main(){
	int x,y,z;
	cin>>x>>y>>z;
	for(int i=x; i<=y; i=i+z){
		int celcious = ((i - 32.0) * 5.0 / 9.0);
		cout<<i <<" "<< celcious <<endl;
	}
}
```

###  Patterns

```cpp
/*-------------------------------CODE------------------------*/
//-----------------PATTERN 1--------------
#include <iostream>
using namespace std;

int main() {
	int n;
	cout << "Enter n"  << endl;
	cin >> n;

	int i = 1;
	while (i <= n) {
		int j = 1;
		while (j <= i) {
			cout << j;
			j = j + 1;
		}
		cout << endl;
		i = i + 1;
	}
}

//-----------------PATTERN 2--------------
#include <iostream>
using namespace std;

int main() {
	int n;
	cout << "Enter n"  << endl;
	cin >> n;

	int i = 1;
	int val = 1;
	while (i <= n) {
		int j = 1;
		while (j <= i) {
			cout << val;
			j = j + 1;
			val = val + 1;
		}
		cout << endl;
		i = i + 1;
	}
}


//-----------------PATTERN 3--------------
#include <iostream>
using namespace std;

int main() {
	int n;
	cout << "Enter n"  << endl;
	cin >> n;

	int i = 1;
	int val = 1;
	while (i <= n) {
		int k = 1;
		while (k <= n - i) {
			cout << " ";
			k = k + 1;
		}

		int j = 1;
		while (j <= i) {
			cout << val;
			j = j + 1;
			val = val + 1;
		}
		cout << endl;
		i = i + 1;
	}
}
```

###  Number Pattern 1

```
Number Pattern 1
 
Print the following pattern
Pattern for N = 4
1
23
345
4567
Input Format :
N (Total no. of rows)
Output Format :
Pattern in N lines
Sample Input 1 :
3
Sample Output 1 :
1
23
345
```

```cpp
/*-------------------------------CODE------------------------*/
// https://classroom.codingninjas.com/app/classroom/me/14886/content/276725/offering/3796230/problem/967

#include<iostream>
using namespace std;


int main(){
	int n; cin>>n;
	int i=1;
	while(i<=n){
		int j=0;
		while(j<i){
			int z=i+j;
			cout<<z;
			j++;
		}
		cout<<endl;
		i++;
	}
}


// 4

// 1
// 23
// 345
// 4567
```

###  Number Pattern 2

```
Number Pattern 2
 
Print the following pattern
Pattern for N = 4


The dots represent spaces.



Input Format :
N (Total no. of rows)
Output Format :
Pattern in N lines
Sample Input :
5
Sample Output :


The dots represent spaces.
```

```cpp
/*-------------------------------CODE------------------------*/
// https://classroom.codingninjas.com/app/classroom/me/14886/content/276725/offering/3796231/problem/968

#include<iostream>
using namespace std;


int main(){
	int n; cin>>n;
	int i=1;
	while(i<=n){
		int j=1;
		while(j<=n-i){
			cout<<" ";
			j++;
		}
		int col=1; int value=i;
		while(col<=i){
			cout<<value;
			value++;
			col++;
		}
		cout<<endl;
		i++;
	}
}

// // 5

//     1
//    23
//   345
//  4567
// 56789

```

###  Start Pattern

```
Start Pattern
 
Print the following pattern
Pattern for N = 4



The dots represent spaces.



Input Format :
N (Total no. of rows)
Output Format :
Pattern in N lines
Constraints :
0 <= N <= 50
Sample Input 1 :
3
Sample Output 1 :
   *
  *** 
 *****
Sample Input 2 :
4
Sample Output 2 :
    *
   *** 
  *****
 *******
```

```cpp
/*-------------------------------CODE------------------------*/
// https://classroom.codingninjas.com/app/classroom/me/14886/content/276725/offering/3796232/problem/969
#include<iostream>
using namespace std;


int main(){
	int n; cin>>n;
	int i=1;
	while(i<=n){
		int j=1;
		while(j<=(n-i)){
			cout<<" ";
			j++;
		}
		int col=1; int value=i;
		while(col<=i){
			cout<< "*";
			if(col<i){
				cout<<"*";
			}
			value++;
			col++;
		}
		cout<<endl;
		i++;
	}
}





// 4

//    *
//   ***
//  *****
// *******

```

###  Total Salary

```
Total Salary
 
Write a program to calculate the total salary of a person. The user has to enter the basic salary (an integer) and the grade (an uppercase character), and depending upon which the total salary is calculated as -
    totalSalary = basic + hra + da + allow – pf
where :
hra   = 20% of basic
da    = 50% of basic
allow = 1700 if grade = ‘A’
allow = 1500 if grade = ‘B’
allow = 1300 if grade = ‘C' or any other character
pf    = 11% of basic.
Round off the total salary and then print the integral part only.
Note: Try finding out a function on the internet to do so
Input format :
Basic salary & Grade (separated by space)
Output Format :
Total Salary
Constraints :
0 <= Basic Salary <= 7,500,000
Sample Input 1 :
10000 A
Sample Output 1 :
17600
Sample Input 2 :
4567 B
Sample Output 2 :
8762
Explanation of Input 2:
We have been given the basic salary as Rs. 4567. We need to calculate the hra, da and pf. 
Now when we calculate each of the, it turns out to be:
hra =  20% of Rs. 4567 = Rs. 913.4
da = 50% od Rs. 4567 = Rs. 2283.5
pf = 11% of Rs. 4567 = Rs. 502.37

Since, the grade is 'B', we take allowance as Rs. 1500.
On substituting these values to the formula of totalSalary, we get Rs. 8761.53 and now rounding it off will result in Rs. 8762 and hence the Answer.
```

```cpp
/*-------------------------------CODE------------------------*/
//https://classroom.codingninjas.com/app/classroom/me/14886/content/276725/offering/3796234/problem/486
#include<iostream>
#include <cmath>
using namespace std;

int main() {
    int basic; cin>> basic;
    char grade; cin>> grade;
    double hra = (basic * 0.2);
    double da= (basic* 0.5);
    double pf = (basic * 0.11);
    int allow, totalSalary;
    if(grade=='A'){
        allow = 1700;
    }else if(grade=='B'){
        allow = 1500;
    }else{
        allow = 1300;
    }
    totalSalary = round(basic + hra + da + allow - pf); 
    cout << totalSalary;

}
```

###  Sum of even & odd

```
Sum of even & odd
 
Write a program to input an integer N and print the sum of all its even digits and sum of all its odd digits separately.
Digits mean numbers, not the places! That is, if the given integer is "13245", even digits are 2 & 4 and odd digits are 1, 3 & 5.
Input format :
 Integer N
Output format :
Sum_of_Even_Digits Sum_of_Odd_Digits
(Print first even sum and then odd sum separated by space)
Constraints
0 <= N <= 10^8
Sample Input 1:
1234
Sample Output 1:
6 4
Sample Input 2:
552245
Sample Output 2:
8 15
Explanation for Input 2:
For the given input, the even digits are 2, 2 and 4 and if we take the sum of these digits it will come out to be 8(2 + 2 + 4) and similarly, if we look at the odd digits, they are, 5, 5 and 5 which makes a sum of 15(5 + 5 + 5). Hence the answer would be, 8(evenSum) <single space> 15(oddSum)
```

```cpp
/*-------------------------------CODE------------------------*/
//https://classroom.codingninjas.com/app/classroom/me/14886/content/276725/offering/3796234/problem/466
#include<iostream>
#include <cmath>
using namespace std;

int main() {
	int num;
	cin>>num;
	int suma=0,sumb=0;
	while(num>0){
		int rand = num % 10;
		// cout<<rand<<endl;
		if(rand%2==0){
			suma +=rand;
		}
		if(rand%2!=0){
			sumb +=rand;
		}
		num = num / 10;
	}
	cout<<  suma << " " <<sumb;

}

// 156230
```

###  Find power of a number

```
Find power of a number
 
Write a program to find x to the power n (i.e. x^n). Take x and n from the user. You need to print the answer.
Note : For this question, you can assume that 0 raised to the power of 0 is 1


Input format :
Two integers x and n (separated by space)
Output Format :
x^n (i.e. x raise to the power n)
Constraints:
0 <= x <= 8 
0 <= n <= 9
Sample Input 1 :
 3 4
Sample Output 1 :
81
Sample Input 2 :
 2 5
Sample Output 2 :
32
```

```cpp
/*-------------------------------CODE------------------------*/
#include<iostream>
#include <cmath>
using namespace std;

int main() {
  
    int x,n;
    cin>>x>>n;
    // cout<< int(pow(x,n));
    int ans=1;
    while(n>0){
        ans = ans * x;
        n--;
    }
    cout<< ans;
}

```


```

Lecture 3 : Conditionals and Loops END HERE

```