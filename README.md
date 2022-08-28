```

Lecture 1 : Flowcharts START HERE

```

# ## Lecture 1 : Flowcharts

---

//============>>>>>>>>>> Lecture 1 : Flowcharts NOTES
[Lecture 1 : Flowcharts NOTES.pdf](https://github.com/karakib2k18/Cpp-Programming-Language-For-DSA/files/9425281/Lecture.1.Flowcharts.NOTES.pdf)

---

```

Lecture 1 : Flowcharts END HERE

```

```

Lecture 2 : Getting Started START HERE

```

# ##Lecture 2 : Getting Started

---

//============>>>>>>>>>> NOTE-Lecture 2 : Getting Started

[Lecture 2 : Getting Started here.pdf](https://github.com/karakib2k18/Cpp-Programming-Language-For-DSA/files/9425307/Lecture.2.Getting.Started.here.pdf)

[Lecture 2 : Getting Started install .pdf](https://github.com/karakib2k18/Cpp-Programming-Language-For-DSA/files/9425309/Lecture.2.Getting.Started.install.pdf)

---

```

Lecture 2 : Getting Started END HERE

```

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

```

Lecture 4: Patterns 1 START HERE

```

# ##Lecture 4: Patterns 1

###  Introduction to Patterns

###  Basic Pattern

###  Code : Square Pattern

```
Code : Square Pattern
 
Print the following pattern for the given N number of rows.
Pattern for N = 4
4444
4444
4444
4444
Input format :
Integer N (Total no. of rows)
Output format :
Pattern in N lines
Constraints
0 <= N <= 50
Sample Input 1:
7
Sample Output 1:
7777777
7777777
7777777
7777777
7777777
7777777
7777777
Sample Input 1:
6
Sample Output 1:
666666
666666
666666
666666
666666
666666
```

```cpp
/*-------------------------------CODE------------------------*/
// https://classroom.codingninjas.com/app/classroom/me/14886/content/276726/offering/3796238/problem/3065
#include<iostream>
using namespace std;


int main(){

       /*  Read input as specified in the question.
	* Print output as specified in the question.
	*/
   int n,i=1;
    cin>>n;
    while(i<=n){
        int j=1;
        while(j<=n){
            cout<< n;
            j++;
        }
        cout<<endl;
        i++;
    }
}
```

###  Square Patterns

```cpp
/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;
int main() {
    int n;
    cin>>n;
    int i=1;
    while(i<=n){
        int j=1;
        while(j<=n){
            cout<<n-j+1;
            j++;
        }
        cout<<endl;
        i++; 
    }
}
```

###  Triangular Patterns

```cpp
/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;
int main() {
    int n;
    cin>>n;
    int i=1;
    int k=1;
    while(i<=n){
        int j=1;
        while(j<=i){
            cout<<k;
            k++;
            j++;
        }
        cout<<endl;
        i++; 
    }
}
```

###  Code : Triangular Star Pattern

```
Code : Triangular Star Pattern
 
Print the following pattern for the given N number of rows.
Pattern for N = 4
*
**
***
****
Note : There are no spaces between the stars (*).
Input format :
Integer N (Total no. of rows)
Output format :
Pattern in N lines
Constraints
0 <= N <= 50
Sample Input 1:
5
Sample Output 1:
*
**
***
****
*****
Sample Input 2:
6
Sample Output 2:
*
**
***
****
*****
******
```

```cpp
/*-------------------------------CODE------------------------*/
//Problem link:  https://classroom.codingninjas.com/app/classroom/me/14886/content/276726/offering/3796241/problem/3066

#include <iostream>
using namespace std;

int main(){
	int n,i=1;
	cin >> n;
	while(i<=n){
		int j=1;
		while(j<=i){
		cout<<"*";
		j++;
		}
		cout<<endl;
		i++;
	}
}

```

###  Code : Triangle Number Pattern

```
Code : Triangle Number Pattern
 
Print the following pattern for the given N number of rows.
Pattern for N = 4
1
22
333
4444
Input format :
Integer N (Total no. of rows)
Output format :
Pattern in N lines
Constraints
0 <= N <= 50
Sample Input 1:
5
Sample Output 1:
1
22
333
4444
55555
Sample Input 2:
6
Sample Output 2:
1
22
333
4444
55555
666666
```

```cpp

/*-------------------------------CODE------------------------*/
//Problem link:  https://classroom.codingninjas.com/app/classroom/me/14886/content/276726/offering/3796242/problem/3067

#include <iostream>
using namespace std;

int main(){
	int n,i=1;
	cin >> n;
	while(i<=n){
		int j=1;
		while(j<=i){
		cout<<i;
		j++;
		}
		cout<<endl;
		i++;
	}
}
```

###  Code : Reverse Number Pattern

```
Code : Reverse Number Pattern
 
Print the following pattern for the given N number of rows.
Pattern for N = 4
1
21
321
4321
Input format :
Integer N (Total no. of rows)
Output format :
Pattern in N lines
Constraints
0 <= N <= 50
Sample Input 1:
5
Sample Output 1:
1
21
321
4321
54321
Sample Input 2:
6
Sample Output 2:
1
21
321
4321
54321
654321
```

```cpp

/*-------------------------------CODE------------------------*/
//Problem link:  https://classroom.codingninjas.com/app/classroom/me/14886/content/276726/offering/3796243/problem/3068

#include <iostream>
using namespace std;

int main(){
	int n,i=1;
	cin >> n;
	while(i<=n){
		int j=i;
		while(j>0){
		cout<<j;
		j--;
		}
		cout<<endl;
		i++;
	}
}

```

###  Character Patterns

```cpp

/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;
int main() {
    int n;
    cin>>n;
    int i=1;
    int k=1;
    while(i<=n){
        int j=1;
        char startChar='A'+i-1;
        while(j<=n){
            char ch=startChar+j-1;
            cout<<ch;
            
            j++;
        }
        cout<<endl;
        i++;  
    }
}
```

###  Code : Alpha Pattern

```
Code : Alpha Pattern
 
Print the following pattern for the given N number of rows.
Pattern for N = 3
 A
 BB
 CCC
Input format :
Integer N (Total no. of rows)
Output format :
Pattern in N lines
Constraints
0 <= N <= 26
Sample Input 1:
7
Sample Output 1:
A
BB
CCC
DDDD
EEEEE
FFFFFF
GGGGGGG
Sample Input 2:
6
Sample Output 2:
A
BB
CCC
DDDD
EEEEE
FFFFFF
```

```cpp

/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;


int main() {
    int n; cin>>n;
    int i= 1;
    while(i<=n){
    	int j=1;
    	while(j<=i){
    		char startchar = 'A'+j-1+i-1;
    		cout<< startchar;
    		j++;
    	}
    	cout<<endl;
        i++;
    }
}
```

###  Code : Character Pattern

```
Code : Character Pattern
 
Print the following pattern for the given N number of rows.
Pattern for N = 4
A
BC
CDE
DEFG
Input format :
Integer N (Total no. of rows)
Output format :
Pattern in N lines
Constraints
0 <= N <= 13
Sample Input 1:
5
Sample Output 1:
A
BC
CDE
DEFG
EFGHI
Sample Input 2:
6
Sample Output 2:
A
BC
CDE
DEFG
EFGHI
FGHIJK
```

```cpp

/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;


int main() {
    int n; cin>>n;
    int i= 1;
    while(i<=n){
    	int j=1;
    	while(j<=i){
    		char startchar = 'A'+j-1+i-1;
    		cout<< startchar;
    		j++;
    	}
    	cout<<endl;
        i++;
    }
}
```

###  Code : Interesting Alphabets

```
Code : Interesting Alphabets
 
Print the following pattern for the given number of rows.
Pattern for N = 5
E
DE
CDE
BCDE
ABCDE
Input format :
N (Total no. of rows)
Output format :
Pattern in N lines
Constraints
0 <= N <= 26
Sample Input 1:
8
Sample Output 1:
H
GH
FGH
EFGH
DEFGH
CDEFGH
BCDEFGH
ABCDEFGH
Sample Input 2:
7
Sample Output 2:
G
FG
EFG
DEFG
CDEFG
BCDEFG
ABCDEFG
```

```cpp
/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;


int main() {
    int n; cin>>n;
    int i= 1;
    int chnum = n;
    while(i<=n){
        int j=1;
        int inc = i;
        while(i>=j){
        char startchar = 'A'+chnum-inc; //a-5-1
        cout<< startchar;
            j++;
            inc--;
        }
        cout<<endl;
        i++;
    }
}
```


```

Lecture 4: Patterns 1 END HERE

```
```

Lecture 5: Patterns 2   START HERE

```

# ##Lecture 5: Patterns 2  

---

//============>>>>>>>>>> Lecture 5: Patterns 2  
[Lecture 5: Patterns 2   Notes.pdf](https://github.com/karakib2k18/Cpp-Programming-Language-For-DSA/files/9434770/Lecture.4.Patterns.2.Notes.pdf)

---

###  Reverse Triangle

```cpp
/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;

int main() {
	int n;
	cin >> n;
	int i = 1;
	while (i <= n) {
		int spaces = 1;
		while (spaces <= n - i) {
			cout << ' ';
			spaces = spaces + 1;
		}

		int stars = 1;
		while (stars <= i) {
			cout << '*';
			stars = stars + 1;
		}
		cout << endl;
		i = i + 1;
	}
}
```

###  Code : Mirror Number Pattern

```
Code : Mirror Number Pattern
 
Print the following pattern for the given N number of rows.
Pattern for N = 4

The dots represent spaces.

Input format :
Integer N (Total no. of rows)
Output format :
Pattern in N lines
Constraints
0 <= N <= 50
Sample Input 1:
3
Sample Output 1:
      1 
    12
  123
Sample Input 2:
4
Sample Output 2:
      1 
    12
  123
1234
```

```cpp
/*

*/

/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;


int main(){
    int n; cin>>n;
    int i=1;
    while(i<=n){
        int j=1;
        int space = n-i;
        while(space>=1){
            cout<< " ";
            space--;
        }
        while(j<=i){
        cout<< j;
            j++;
        }
        cout<<endl;
        i++;
    }
}

```

###  Code : Mirror Number Pattern

```

```

```cpp
/*

*/

/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;

int main() {
	int n;
	cin >> n;
	int i = 1;
	while (i <= n) {
		int j = 1;
		while (j <= n - i + 1) {
			cout << '*';
			j = j + 1;
		}
		cout << endl;
		i = i + 1;
	}
}

```

###  Code : Inverted Number Pattern

```
Code : Inverted Number Pattern
 
Print the following pattern for the given N number of rows.
Pattern for N = 4
4444
333
22
1
Input format :
Integer N (Total no. of rows)
Output format :
Pattern in N lines
Constraints :
0 <= N <= 50
Sample Input 1:
5
Sample Output 1:
55555 
4444
333
22
1
Sample Input 2:
6
Sample Output 2:
666666
55555 
4444
333
22
1
```

```cpp
/*

*/

/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;


int main(){

    int n; cin>>n;
    int i=n;
    while(i>=1){
        int j=1;
        // int space = n-i;
        // while(space>=1){
        //     cout<< " ";
        //     space--;
        // }
        while(j<=i){
        cout<< i;
            j++;
        }
        cout<<endl;
        i--;
    }
}

```

###  Isosceles Triangle

```

```

```cpp
/*

*/

/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;

int main() {
	int n;
	cin >> n;
	int i = 1;
	while (i <= n) {
		int spaces = 1;
		while (spaces <= n - i) {
			cout << ' ';
			spaces = spaces + 1;
		}

		int j = 1;
		while (j <= i) {
			cout << j;
			j = j + 1;
		}

		j = i - 1;
		while (j >= 1) {
			cout << j;
			j = j - 1;
		}
		cout << endl;
		i = i + 1;
	}
}
```

###  Code : Star Pattern

```
Code : Star Pattern
 
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
/*

*/

/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;


int main(){
    int n; cin>>n;
    int i=1;
    while(i<=n){
        int j=1;
        int space = n-i;
        while(space>=1){
            cout<< " ";
            space--;
        }
        while(j<=i){
        cout<< "*";
            if(j<i){
               cout<< "*"; 
            }
            j++;
        }
        cout<<endl;
        i++;
    }
}
```

###  Code : Triangle of Numbers

```
Code : Triangle of Numbers
 
Print the following pattern for the given number of rows.
Pattern for N = 4



The dots represent spaces.



Input format :
Integer N (Total no. of rows)
Output format :
Pattern in N lines
Constraints :
0 <= N <= 50
Sample Input 1:
5
Sample Output 1:
           1
         232
       34543
     4567654
   567898765
Sample Input 2:
4
Sample Output 2:
           1
         232
       34543
     4567654
```

```cpp
/*

*/

/*-------------------------------CODE------------------------*/

#include<iostream>
using namespace std;


int main(){
    int n; cin>>n;
    int i=1;
    while(i<=n){
        int space = n-i;
        while(space>=1){
            cout<< " ";
            space--;
        }
        int j=1;
        while(j<=i){
            cout<< i+j-1;
            j++;
        }
        j=2*(i-1);
        while(j>=i){
            cout<< j;
            j--;
        }
        cout<<endl;
        i++;
    } 
}



/* //2nd way

#include<iostream>
using namespace std;


int main(){
    int n; cin>>n;
    int i=1;
    while(i<=n){
        int space = n-i;
        while(space>=1){
            cout<< " ";
            space--;
        }
        int j=1;
        while(j<=i){
            cout<< i+j-1;
            j++;
        }
        j=i-1;
        while(j>=1){
            cout<< i+j-1;
            j--;
        }
        cout<<endl;
        i++;
    }
}
*/
```

###  Code : Diamond of stars

```
Code : Diamond of stars
 
Print the following pattern for the given number of rows.
Note: N is always odd.

Pattern for N = 5

The dots represent spaces.

Input format :
N (Total no. of rows and can only be odd)
Output format :
Pattern in N lines
Constraints :
1 <= N <= 49
Sample Input 1:
5
Sample Output 1:
  *
 ***
*****
 ***
  *
Sample Input 2:
3
Sample Output 2:
  *
 ***
  *
```

```cpp
/*

*/

/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;

int main(){
    int n; cin>>n;
    
    int newn = (n/2+1);
    for(int i=1; i<=newn; i++){
        for(int space = newn-i; space>=1;  space--){
            cout<< " ";
        }
        // int space = newn-i;
        // while(space>=1){
        //     space--;
        // }
        for(int j=1; j<=i; j++ ){
            cout<< "*";
        }
        for(int j=i; j>1; j-- ){
            cout<< "*";
        }
        cout<<endl;
    }
    for(int i=newn-1; i>=1 ; i--){
        for(int space = newn-i; space>=1;  space--){
            cout<< " ";
        }
        for(int j=1; j<=i; j++ ){
            cout<< "*";
        }
        for(int j=i; j>1; j-- ){
            cout<< "*";
        }
        cout<<endl;
    }
}
```

```

Lecture 5: Patterns 2   END HERE

```


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

```

Lecture 6.5 : Test 1 START HERE

```

# ##Lecture 6.5 : Test 1

### Pyramid Number Pattern

```
Pyramid Number Pattern
 
Print the following pattern for the given number of rows.
Pattern for N = 4
   1
  212
 32123
4321234
Input format : N (Total no. of rows)

Output format : Pattern in N lines

Sample Input :
5
Sample Output :
        1
      212
    32123
  4321234
543212345
```

```cpp
/*

*/

/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;

int main(){

  // Write your code here  
    int n; cin>>n;
    int i=1;
    while(i<=n){
        int space = n-i;
        while(space>=1){
            cout<< " ";
            space--;
        }
        int j=i;
        while(j>1){
            cout<< j;
            j--;
        }
                 j=1;
        while(j<=i){
            cout<< j;
            j++;
        }
        // j=2*(i-1);
        // while(j>=i){
        //     cout<< j;
        //     j--;
        // }
        cout<<endl;
        i++;
    }
}
```

### Number Star Pattern

```
Number Star Pattern
 
Print the following pattern for given number of rows.
Input format :

Line 1 : N (Total number of rows)

Sample Input :
   5
Sample Output :
1234554321
1234**4321
123****321
12******21
1********1
```

```cpp
/*

*/

/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;


int main(){

    int n; cin>>n;
    int i=1;
    while(i<=n){
        int j=1;
        while(j<=n-i+1){
            cout<< j;
            j++;
        }
        int space = i;
        while(space>1){
            cout<< "*";
            space--;
        }
         space = i;
        while(space>1){
            cout<< "*";
            space--;
        }
        j=n-i+1;
        while(j>=1){
            cout<< j;
            j--;
        }
        cout<<endl;
        i++;
    }
}

```

### Second Largest

```
Second Largest
 
Take input a stream of n integer elements, find the second largest element present.
The given elements can contain duplicate elements as well. If only 0 or 1 element is given, the second largest should be INT_MIN ( - 2^31 ).
Input format :

Line 1 : Total number of elements (n)

Line 2 : N elements (separated by space)

Sample Input 1:
 4
 3 9 0 9
Sample Output 1:
 3
Sample Input 2 :
 2
 4 4
Sample Output 2:
 -2147483648
Sample Output Explanation:
Since both the elements are equal here, hence second largest element is INT_MIN i.e. ( -2^31 )
```

```cpp
/*

*/

/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;
#include <climits>


int main(){
    
    // Write your code here
    
    int n, i;
    cin  >> n;
    
    int arr[n];
    
    //Input array elements
    for (i = 0; i < n; i++) {
        cin >> arr[i];
    }
    
    //Assign min value to max and second_max
    int max         = INT_MIN;
    int second_max  = INT_MIN;

    for (i = 0; i < n; i++) {
        
        if(arr[i] > max) {
            second_max = max;
            max        = arr[i];
        }
        
        if(arr[i] < max && arr[i] > second_max) {
            second_max = arr[i];
        }
    }
    
    cout <<  second_max;
    return 0;
}
```

```

Lecture 6.5 : Test 1 END HERE

```

```

Lecture 7: Functions  START HERE

```

# ##Lecture 7: Functions 

---

//============>>>>>>>>>> Lecture 7: Functions 
[Lecture 7: Functions NOTES.pdf](https://github.com/karakib2k18/Cpp-Programming-Language-For-DSA/files/9434917/Lecture.7.Functions.NOTES.pdf)

---

### What are Functions ?

 

```cpp
 

/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;

void print_1_to_n(int n) {
	for(int i = 1; i<=n; i++) {
		cout << i << endl;
	}
}

int main() {
	print_1_to_n(10);
}

//------------------------------------
#include <iostream>
using namespace std;

bool isPrime(int n) {
	int d = 2;
	while (d < n) {
		if (n % d == 0) {
			return false;
		}
		d++;
	}
	return true;
}

int main() {
	bool ans = isPrime(31);
	cout << ans << endl;
	ans = isPrime(85);
	cout << ans << endl;
}

//-----------------------------------------
#include <iostream>
using namespace std;

int factorial(int n) {
	int ans = 1;
	int i = 1;
	while (i <= n) {
		ans = ans * i;
		i++;
	}
	return ans;
}

int main() {
	int n, r;
	cin >> n >> r;
	
	int fact_n = factorial(n);
	int fact_r = factorial(r);
	int fact_n_r = factorial(n - r);
	int ans = fact_n/(fact_r * fact_n_r);
	cout << ans << endl;
	

	/*
	int fact_n = 1;
	int i = 1;
	while (i <= n) {
		fact_n = fact_n * i;
		i++;
	}

	int fact_r = 1;
	i = 1;
	while (i <= r) {
		fact_r = fact_r * i;
		i++;
	}

	int fact_n_r = 1;
	i = 1;
	while (i <= n - r) {
		fact_n_r = fact_n_r * i;
		i++;
	}
	cout << fact_n/(fact_r * fact_n_r) << endl;
	*/
}

```

### Fahrenheit to Celsius Table

```
Fahrenheit to Celsius Table
 
Given three values - Start Fahrenheit Value (S), End Fahrenheit value (E) and Step Size (W), you need to convert all Fahrenheit values from Start to End at the gap of W, into their corresponding Celsius values and print the table.
Input Format :
3 integers - S, E and W respectively
Output Format :
Fahrenheit to Celsius conversion table. One line for every Fahrenheit and Celsius Fahrenheit value. Fahrenheit value and its corresponding Celsius value should be separate by tab ("\t")
Constraints :
0 <= S <= 1000
0 <= E <= 1000
0 <= W <= 1000
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
120 
200 
40
Sample Output 2:
120 48
160 71
200 93
Explanation for Sample Output 2 :
Start value is 120, end value is 200 and step size is 40. Therefore, the values we need to convert are 120, 120 + 40 = 160, and 160 + 40 = 200. 
The formula for converting Fahrenheit to Celsius is:
Celsius Value = (5/9)*(Fahrenheit Value - 32)  
Plugging 120 into the formula, the celsius value will be (5 / 9)*(120 - 32) => (5 / 9) * 88 => (5 * 88) / 9 => 440 / 9 => 48.88
But we'll only print 48 because we are only interested in the integral part of the value.
```

```cpp
/*
#include<iostream>
using namespace std;
#include "Solution.h"

int main(){
    int start, end, step;
    cin >> start >> end >> step;
  
    printTable(start, end, step);

}
*/

/*-------------------------------CODE------------------------*/
void printTable(int start, int end, int step)
{
	int currentValue = start;
	while (currentValue <= end)
	{
		int celsiusValue = (int)((5.0 / 9) *(currentValue - 32));
		cout << currentValue << "\t" << celsiusValue << endl;
		currentValue += step;
	}
}
```

###  Fibonacci Number

```
Fibonacci Number
 
Given a number N, figure out if it is a member of fibonacci series or not. Return true if the number is member of fibonacci series else false.
Fibonacci Series is defined by the recurrence
    F(n) = F(n-1) + F(n-2)
where F(0) = 0 and F(1) = 1


Input Format :
Integer N
Output Format :
true or false
Constraints :
0 <= n <= 10^4
Sample Input 1 :
5
Sample Output 1 :
true
Sample Input 2 :
14
Sample Output 2 :
false    
```

```cpp
/*
#include<iostream>
using namespace std;
#include "Solution.h"

int main(){

  int n; 
  cin >> n ;
  if(checkMember(n)){
    cout << "true" << endl;
  }else{
    cout << "false" << endl;
  }

}

*/

/*-------------------------------CODE------------------------*/

bool checkMember(int n){

    int a = 0;
    int b = 1;
    int c;
    while(a < n){
        c = a + b;
        a = b;
        b = c;
    }
    return a == n; //This statement will return true if 'a' is equal to 'n', false otherwise.
}

```

### How Function Calling Works ?

 

```cpp
 

/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;

void B() {
	cout << 5 << endl;
}

void A(int a) {
	cout << 1 << endl;
	B();
	cout << 2 << endl;
}

int main() {
	int n = 10;
	cout << 3 << endl;
	A(n);
	cout << n << endl;
	cout << 4 << endl;
}

//----------------------------------
#include <iostream>
using namespace std;

bool isPrime(int n) {
	int d = 2;
	while (d < n) {
		if (n % d == 0) {
			return false;
		}
		d++;
	}
	return true;
}

int main() {
	int n;
	cin >> n;
	for (int x = 2; x <= n; x++) {
		if (isPrime(x)) {
			cout << x << endl;
		}
	}
}

```

### Variables and Scopes

 

```cpp
 

/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;

int fact(int n) {
	//cout << a << endl;
	int ans = 1;
	for (int i = 1; i <=n ;i++) {
		ans = ans * i;
	}
	return ans;
}

int main() {
	int a;
	cin >> a;
	int output = fact(a);
	//cout << ans << endl;
	//cout << n << endl;
	cout << output << endl;
}

```

### Pass By Value

 

```cpp
 

/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;

void increment(int a) {
	a = a + 1;
}

int main() {
	int a = 10;
	increment(a);
	cout << a << endl;
}
```


```

Lecture 7: Functions  END HERE

```

```

Lecture 8: Arrays START HERE

```

# ##Lecture 8: Arrays

---

//============>>>>>>>>>> Lecture 8: Arrays
[Lecture 8: Arrays Notes.pdf](https://github.com/karakib2k18/Cpp-Programming-Language-For-DSA/files/9436501/Lecture.8.Arrays.Notes.pdf)

---

###  What are Arrays ?

 

```cpp
 

/*-------------------------------CODE------------------------*/

```

###  More on Arrays

 

```cpp
 

/*-------------------------------CODE------------------------*/
#include <iostream>
#include <climits>
using namespace std;

int main() {
	// Take array input from the user

	int n;
	cin >> n;

	int input[100];
	
	for(int i = 0; i < n; i++) {
		cin >> input[i];
	}

	// Print array
	for(int i = 0; i < n; i++) {
		cout << input[i] << endl;
	}

	// Largest velement in the array

	int max = INT_MIN;

	for(int i = 0; i < n; i++) {
		if(input[i] > max) {
			max = input[i];
		}
	}

	cout << "Max : " << max << endl;

}
```

###  Array Sum

```
Array Sum
 
Given an array of length N, you need to find and print the sum of all elements of the array.
Input Format :
Line 1 : An Integer N i.e. size of array
Line 2 : N integers which are elements of the array, separated by spaces
Output Format :
Sum
Constraints :
1 <= N <= 10^6
Sample Input :
3
9 8 9
Sample Output :
26
```

```cpp
 

/*-------------------------------CODE------------------------*/
#include<iostream> 
using namespace std;

int main(){ 
    int size; 
    cin >> size; 
    int arr[1000000]; 
    
    for(int i = 0; i < size; i++){ 
        cin >> arr[i]; 
    } 
    
    int result = 0; 
    for(int i = 0; i < size; i++){ 
        result += arr[i]; 
    } 
    cout << result << endl; 
}
```

###  How are Arrays Stored ?

 

```cpp
 

/*-------------------------------CODE------------------------*/
#include <iostream>
#include <climits>
using namespace std;

int main() {
	// Take array input from the user

	int n;
	cin >> n;

	int input[100];
	
	for(int i = 0; i < n; i++) {
		cin >> input[i];
	}

	// Print array
	for(int i = 0; i < n; i++) {
		cout << input[i] << endl;
	}

	// Largest velement in the array

	int max = INT_MIN;

	for(int i = 0; i < n; i++) {
		if(input[i] > max) {
			max = input[i];
		}
	}
	cout << "Max : " << max << endl;
}
```

###  Linear Search

```
Linear Search
 
You have been given a random integer array/list(ARR) of size N, and an integer X. You need to search for the integer X in the given array/list using 'Linear Search'.
 You have been required to return the index at which X is present in the array/list. If X has multiple occurrences in the array/list, then you need to return the index at which the first occurrence of X would be encountered. In case X is not present in the array/list, then return -1.
'Linear search' is a method for finding an element within an array/list. It sequentially checks each element of the array/list until a match is found or the whole array/list has been searched.
Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains an integer 'N' representing the size of the array/list.

Second line contains 'N' single space separated integers representing the elements in the array/list.

Third line contains the value of X(integer to be searched in the given array/list)
Output format :
For each test case, print the index at which X is present or -1, otherwise.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^5
-2 ^ 31 <= X <= (2 ^ 31) - 1
Time Limit: 1 sec
Sample Input 1:
1
7
2 13 4 1 3 6 28
3
Sample Output 1:
4
Sample Input 2:
2
7
2 13 4 1 3 6 28
9
5
7 8 5 9 5      
5
Sample Output 2:
-1
2
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{
	int t;
	cin >> t;
	while (t--)
	{
		int n;
		cin >> n;
		int *arr = new int[n];
		for (int i = 0; i < n; ++i)
		{
			cin >> arr[i];
		}
		int val;
		cin >> val;
		cout << linearSearch(arr, n, val) << endl;
	}
	return 0;
}
*/

/*-------------------------------CODE------------------------*/
int linearSearch(int *arr, int n, int val)
{
	for (int i = 0; i < n; i++)
	{
		if (arr[i] == val)
		{
			return i;
		}
	}
	return -1;
}
```

###  Arrange Numbers in Array

```
Arrange Numbers in Array
 
You have been given an empty array(ARR) and its size N. The only input taken from the user will be N and you need not worry about the array.
Your task is to populate the array using the integer values in the range 1 to N(both inclusive) in the order - 1,3,5,.......,6,4,2.
Note:
You need not print the array. You only need to populate it.
Input Format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

The first and the only line of each test case or query contains an integer 'N'.
Output Format :
For each test case, print the elements of the array/list separated by a single space.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^4

Time Limit: 1sec
Sample Input 1 :
1
6
Sample Output 1 :
1 3 5 6 4 2
Explanation of Sample Input 1 :
Since the value of N is 6, the number will be stored in the array in such a fashion that 1 will appear at 0th index, then 2 at the last index, in a similar fashion 3 is stored at index 1. Hence the array becomes 1 3 5 6 4 2.
Sample Input 2 :
2
9
3
Sample Output 2 :
1 3 5 7 9 8 6 4 2
1 3 2
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{
	int t;
	cin >> t;
	while (t--)
	{
		int n;
		cin >> n;

		int *arr = new int[n];
		arrange(arr, n);
		for (int i = 0; i < n; i++)
		{
			cout << arr[i] << " ";
		}
		cout << endl;
		delete [] arr;
	}	
}
*/

/*-------------------------------CODE------------------------*/
void arrange(int *arr, int n)
{
//         for(int i=0;i<n;i++)
//         {
//             arr[i]=n;
//         }
//         for(int i=0;i<n/2;i++)
//         {
//             arr[i]=2*i+1;
//             arr[n-1-i]=2*i+2;
//         }
        
//         cout<< arr<<endl;
    
    int val=1;
    int start = 0 ,end = n-1;
    while(start<=end){
        if(val%2==1){
            arr[start]=val;
            val++;
            start++;
          } else{
            arr[end]=val;
            val++;
            end--;
        }
    }
}
```

###  Passing Arrays to Functions

 

```cpp
 

/*-------------------------------CODE------------------------*/
#include <iostream>
#include <climits>
using namespace std;

void printArray(int input[], int n) {
	for(int i = 0; i < n; i++) {
		cout << input[i] << " ";
	}
	cout << endl;
}

void increment(int a, int b[], int n) {
	a++;
	b[0]++;
}

void reverse(int input[], int n) {
	int i = 0, j = n - 1;
	while(i < j) {
		int temp = input[i];
		input[i] = input[j];
		input[j] =temp;
		i++;
		j--;
	}
}


int main() {

	int a = 10;
	int b[10] = {1, 2, 3, 4, 5};
	reverse(b, 5);
	printArray(b, 5);

	/*
	increment(a, b, 10);

	cout << "a : " << a << endl;
	cout << "b[0] : " << b[0] << endl;
	*/
	
	//	int input[100] = {1, 2, 3};
	
	/*
	// Take array input from the user
	int n;
	cin >> n;
	for(int i = 0; i < n; i++) {
		cin >> input[i];
	}*/

//	printArray(b, 100);

}
```

###  Swap Alternate

```
Swap Alternate
 
You have been given an array/list(ARR) of size N. You need to swap every pair of alternate elements in the array/list.
You don't need to print or return anything, just change in the input array itself.
Input Format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains an integer 'N' representing the size of the array/list.

Second line contains 'N' single space separated integers representing the elements in the array/list.
Output Format :
For each test case, print the elements of the resulting array in a single row separated by a single space.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^5
Time Limit: 1sec
Sample Input 1:
1
6
9 3 6 12 4 32
Sample Output 1 :
3 9 12 6 32 4
Sample Input 2:
2
9
9 3 6 12 4 32 5 11 19
4
1 2 3 4
Sample Output 2 :
3 9 12 6 32 4 11 5 19 
2 1 4 3 
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{
	int t;
	cin >> t;
	while (t--)
	{
		int size;
		cin >> size;
		int *arr = new int[size];
		for (int i = 0; i < size; i++)
		{
			cin >> arr[i];
		}
		swapAlternate(arr, size);
		for (int i = 0; i < size; i++)
		{
			cout << arr[i] << " ";
		}
		cout << endl;
		delete [] arr;
	}
}
*/

/*-------------------------------CODE------------------------*/
void swapAlternate(int *arr, int size)
{
    //Write your code here
    for(int i=0; i<size-1; i+=2){
        int temp = arr[i];
        arr[i]=arr[i+1];
        arr[i+1]=temp;
    }
}
```

###  Find Unique

```
Find Unique
 
You have been given an integer array/list(ARR) of size N. Where N is equal to [2M + 1].
Now, in the given array/list, 'M' numbers are present twice and one number is present only once.
You need to find and return that number which is unique in the array/list.
 Note:
Unique element is always present in the array/list according to the given condition.
Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains an integer 'N' representing the size of the array/list.

Second line contains 'N' single space separated integers representing the elements in the array/list.
Output Format :
For each test case, print the unique element present in the array.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^3
Time Limit: 1 sec
Sample Input 1:
1
7
2 3 1 6 3 6 2
Sample Output 1:
1
Sample Input 2:
2
5
2 4 7 2 7
9
1 3 1 3 6 6 7 10 7
Sample Output 2:
4
10
```

```cpp
/*
#include <iostream>
#include "solution.h"
using namespace std;

int main()
{

	int t;
	cin >> t;

	while (t--)
	{
		int size;
		cin >> size;
		int *input = new int[size];

		for (int i = 0; i < size; ++i)
		{
			cin >> input[i];
		}

		cout << findUnique(input, size) << endl;
	}

	return 0;
}
*/

/*-------------------------------CODE------------------------*/
int findUnique(int *arr, int size)
{
    /*
    //1st APPROACH
    // O(n^2)
	for(int i=0; i<size; ++i){
        for(int j=0;j<size; ++j){
            if(i != j && arr[i] == arr[j]){
            	break;
            }
        }
        
        if(j==size){
        	return arr[i];    
        }
	}
   */
    
    //2nd APPROACH

    //Now XOR is associative and commutative, so I can write it as:
    //Answer = (2^2) ^ (3^3) ^ 1 ^ (6 ^ 6) = 0 ^ 0 ^ 1 ^ 0 = 1
    // O(n)
    int res = 0, i;
    for (i = 0; i < size; i++){
	    res ^= arr[i];
    }
    return res;
}
```

###  Find Duplicate

```
Find Duplicate
 
You have been given an integer array/list(ARR) of size N which contains numbers from 0 to (N - 2). Each number is present at least once. That is, if N = 5, the array/list constitutes values ranging from 0 to 3 and among these, there is a single integer value that is present twice. You need to find and return that duplicate number present in the array.
Note :
Duplicate number is always present in the given array/list.
Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains an integer 'N' representing the size of the array/list.

Second line contains 'N' single space separated integers representing the elements in the array/list.
Output Format :
For each test case, print the duplicate element in the array/list.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^3
Time Limit: 1 sec
Sample Input 1:
1
9
0 7 2 5 4 7 1 3 6
Sample Output 1:
7
Sample Input 2:
2
5
0 2 1 3 1
7
0 3 1 5 4 3 2
Sample Output 2:
1
3
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{

	int t;
	cin >> t;
	
	while (t--)
	{
		int size;
		cin >> size;
		int *input = new int[size];

		for (int i = 0; i < size; i++)
		{
			cin >> input[i];
		}

		cout << duplicateNumber(input, size) << endl;
	}

	return 0;
}
*/

/*-------------------------------CODE------------------------*/
int duplicateNumber(int *arr, int size)
{
    for(int i=0; i<size; ++i){ 
        for(int j=i+1;j<size; ++j){
            if( arr[i] == arr[j]){
                return arr[i];
            }
        }
    }
}
```

###  Intersection of Two Arrays II

```
Intersection of Two Arrays II
 
You have been given two integer arrays/list(ARR1 and ARR2) of size N and M, respectively. You need to print their intersection; An intersection for this problem can be defined when both the arrays/lists contain a particular value or to put it in other words, when there is a common value that exists in both the arrays/lists.
Note :
Input arrays/lists can contain duplicate elements.

The intersection elements printed would be in the order they appear in the first array/list(ARR1)


Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains an integer 'N' representing the size of the first array/list.

Second line contains 'N' single space separated integers representing the elements of the first the array/list.

Third line contains an integer 'M' representing the size of the second array/list.

Fourth line contains 'M' single space separated integers representing the elements of the second array/list.
Output format :
For each test case, print the intersection elements in a row, separated by a single space.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^5
0 <= M <= 10^5
Time Limit: 1 sec 
Sample Input 1 :
2
6
2 6 8 5 4 3
4
2 3 4 7 
2
10 10
1
10
Sample Output 1 :
2 4 3
10
Sample Input 2 :
1
4
2 6 1 2
5
1 2 3 4 2
Sample Output 2 :
2 1 2
Explanation for Sample Output 2 :
Since, both input arrays have two '2's, the intersection of the arrays also have two '2's. The first '2' of first array matches with the first '2' of the second array. Similarly, the second '2' of the first array matches with the second '2' if the second array.
```

```cpp
/*
#include <iostream>
#include <algorithm>
using namespace std;
#include "solution.h"

int main()
{
	int t;
	cin >> t;
	while (t--)
	{

		int size1, size2;

		cin >> size1;
		int *input1 = new int[size1];

		for (int i = 0; i < size1; i++)
		{
			cin >> input1[i];
		}

		cin >> size2;
		int *input2 = new int[size2];

		for (int i = 0; i < size2; i++)
		{
			cin >> input2[i];
		}

		intersection(input1, input2, size1, size2);
		
		delete[] input1;
		delete[] input2;
		
		cout << endl;
	}

	return 0;
}
*/

/*-------------------------------CODE------------------------*/
#include<climits>
void intersection(int *input1, int *input2, int size1, int size2)
{
    //Write your code here
    for(int i=0; i<size1; ++i){
        for(int j=0;j<size2; ++j){
            if( input1[i] == input2[j]){
                cout<< input1[i]<<" ";
                input2[j] = INT_MAX ;
                break;
            }
        }
	}
}
```

###  Pair Sum

```
Pair Sum
 
You have been given an integer array/list(ARR) and a number X. Find and return the total number of pairs in the array/list which sum to X.
Note:
Given array/list can contain duplicate elements. 
Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains an integer 'N' representing the size of the first array/list.

Second line contains 'N' single space separated integers representing the elements in the array/list.

Third line contains an integer 'X'.
Output format :
For each test case, print the total number of pairs present in the array/list.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^3
0 <= X <= 10^9
Time Limit: 1 sec
Sample Input 1:
1
9
1 3 6 2 5 4 3 2 4
7
Sample Output 1:
7
Sample Input 2:
2
9
1 3 6 2 5 4 3 2 4
12
6
2 8 10 5 -2 5
10
Sample Output 2:
0
2


 Explanation for Input 2:
Since there doesn't exist any pair with sum equal to 12 for the first query, we print 0.

For the second query, we have 2 pairs in total that sum up to 10. They are, (2, 8) and (5, 5).
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{
	int t;
	cin >> t;

	while (t--)
	{
		int size;
		int x;

		cin >> size;
		int *input = new int[size];

		for (int i = 0; i < size; i++)
		{
			cin >> input[i];
		}

		cin >> x;

		cout << pairSum(input, size, x) << endl;

		delete[] input;
	}
	
	return 0;
}
*/

/*-------------------------------CODE------------------------*/
int pairSum(int *input, int size, int x)
{
	int numPairs = 0;
	for (int i = 0; i < size; i++)
	{
		for (int j = i + 1; j < size; j++)
		{
			if (input[i] + input[j] == x)
			{ 	++numPairs;
			}
		}
	}
	return numPairs;
}
```

###  Triplet Sum

```
Triplet Sum
 
You have been given a random integer array/list(ARR) and a number X. Find and return the number of triplets in the array/list which sum to X.
Note :
Given array/list can contain duplicate elements.
Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains an integer 'N' representing the size of the first array/list.

Second line contains 'N' single space separated integers representing the elements in the array/list.

Third line contains an integer 'X'.
Output format :
For each test case, print the total number of triplets present in the array/list.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 50
0 <= N <= 10^2
0 <= X <= 10^9
Time Limit: 1 sec
Sample Input 1:
1
7
1 2 3 4 5 6 7 
12
Sample Output 1:
5
Sample Input 2:
2
7
1 2 3 4 5 6 7 
19
9
2 -5 8 -6 0 5 10 11 -3
10
Sample Output 2:
0
5


 Explanation for Input 2:
Since there doesn't exist any triplet with sum equal to 19 for the first query, we print 0.

For the second query, we have 5 triplets in total that sum up to 10. They are, (2, 8, 0), (2, 11, -3), (-5, 5, 10), (8, 5, -3) and (-6, 5, 11)
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{
	int t;
	cin >> t;

	while (t--)
	{
		int size;
		int x;
		cin >> size;

		int *input = new int[size];

		for (int i = 0; i < size; i++)
		{
			cin >> input[i];
		}
		cin >> x;

		cout << tripletSum(input, size, x) << endl;

		delete[] input;
	}

	return 0;
}
*/

/*-------------------------------CODE------------------------*/
int tripletSum(int *input, int size, int x)
{
	int numTriplets = 0;
	for (int i = 0; i < size; i++)
	{
		for (int j = i + 1; j < size; j++)
		{
			for (int k = j + 1; k < size; k++)
			{
				if (input[i] + input[j] + input[k] == x)
				{ 		++numTriplets;
				}
			}
		}
	}
	return numTriplets;
}
```

###  Sort 0 1

```
Sort 0 1
 
You have been given an integer array/list(ARR) of size N that contains only integers, 0 and 1. Write a function to sort this array/list. Think of a solution which scans the array/list only once and don't require use of an extra array/list.
Note:
You need to change in the given array/list itself. Hence, no need to return or print anything. 
Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains an integer 'N' representing the size of the array/list.

Second line contains 'N' single space separated integers(all 0s and 1s) representing the elements in the array/list.
Output format :
For each test case, print the sorted array/list elements in a row separated by a single space.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^5
Time Limit: 1 sec
Sample Input 1:
1
7
0 1 1 0 1 0 1
Sample Output 1:
0 0 0 1 1 1 1
Sample Input 2:
2
8
1 0 1 1 0 1 0 1
5
0 1 0 1 0
Sample Output 2:
0 0 0 1 1 1 1 1
0 0 0 1 1 
```

```cpp
/*
#include <iostream>
#include <algorithm>
using namespace std;

#include "solution.h"

int main()
{

	int t;
	cin >> t;

	while (t--)
	{
		int size;

		cin >> size;
		int *input = new int[size];

		for (int i = 0; i < size; ++i)
		{
			cin >> input[i];
		}

		sortZeroesAndOne(input, size);

		for (int i = 0; i < size; ++i)
		{
			cout << input[i] << " ";
		}

		cout << endl;
		delete[] input;
	}

	return 0;
}
*/

/*-------------------------------CODE------------------------*/
/*
//-------------------- 1ST APPROACH-----------------------
void sortZeroesAndOne(int input[], int size) { 
    int j = 0;
    for(int i=0; i<size; i++){
        if(input[i]==0){
            int temp = input[j];
            input[j]=input[i];
            input[i] = temp;
            j++;
        }
    }
}
*/

// -----------------------2nd APPROACH------------------------
void sortZeroesAndOne(int input[], int size) { 
    // i first theke and j last theke start;
    // then first a jodi 1 pai tahole sheta last er sathe swap kore pelbo. 
    //then last-- kore pelte hobe. if !=1 then i++ korte hobe. 
    
    int i=0;
    int j=size-1;
    
    while(i<=j){
        //if 1
        if(input[i]==1){
            int temp = input[j];
            input[j] = input[i];
            input[i] = temp;
            j--;
            
        //if 0
        }else{
            i++;
        }
    }
}

```

```

Lecture 8: Arrays END HERE

```

```

Lecture 9: Searching and Sorting START HERE

```

# ##Lecture 9: Searching and Sorting

---

//============>>>>>>>>>> Lecture 9: Searching and Sorting
[Lecture 9: Searching and Sorting Notes.pdf](https://github.com/karakib2k18/Cpp-Programming-Language-For-DSA/files/9437865/Lecture.9.Searching.and.Sorting.Notes.pdf)

---

###  Understanding Binary Search

![image](https://user-images.githubusercontent.com/57065763/187023901-dce357a6-9803-4ed1-8721-e6f455c3f96b.png)

###  Code Binary Search

```
Code Binary Search
 
You have been given a sorted(in ascending order) integer array/list(ARR) of size N and an element X. Write a function to search this element in the given input array/list using 'Binary Search'. Return the index of the element in the input array/list. In case the element is not present in the array/list, then return -1.
Input format :
The first line contains an Integer 'N' which denotes the size of the array/list.

Second line contains 'N' single space separated integers representing the elements in the array/list.

Third line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow..

All the 't' lines henceforth, will take the value of X to be searched for in the array/list.
Output Format :
For each test case, print the index at which X is present, -1 otherwise.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^4
0 <= N <= 10^6
0 <= X <= 10^9
Time Limit: 1 sec
Sample Input 1:
7
1 3 7 9 11 12 45
1
3
Sample Output 1:
1
Sample Input 2:
7
1 2 3 4 5 6 7
2
9
7
Sample Output 2:
-1
6
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{

	int size;
	cin >> size;
	int *input = new int[size];

	for(int i = 0; i < size; ++i)
	{
		cin >> input[i];
	}
	
	int t;
	cin >> t;

	while (t--)
	{
		int val;
		cin >> val;
		cout << binarySearch(input, size, val) << endl;
	}
	
	delete [] input;
	return 0;
}
*/

/*-------------------------------CODE------------------------*/
int binarySearch(int *input, int n, int val)
{
    int start = 0, end = n-1, mid;
    
    while(start<=end){
        mid = start+(end-start)/2;
        
        if(input[mid]<val){ //value mid theke boro
            start = mid+1;
        }else if(input[mid]>val){ //value mid theke choto
            end = mid-1;
        }else{
            return mid;
        }
    }
    return -1;
}
```

###  Binary Search
![image](https://user-images.githubusercontent.com/57065763/187024245-40c377cf-ff83-4f91-acce-4d7c1ce4ad39.png)

 

```cpp
 

/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;

int binarySearch(int arr[], int n, int x) {
	int start = 0, end = n - 1;
	while(start <= end) {
		int mid = (start + end) / 2;
		if(arr[mid] == x) {
			return mid;
		}
		else if(x < arr[mid]) {
			end = mid - 1;
		}
		else {
			start = mid + 1;
		}
	}

	return -1;
}

int main() {
	// Take array input from the user
	int n;
	cin >> n;

	int input[100];
	
	for(int i = 0; i < n; i++) {
		cin >> input[i];
	}

	int x;
	cin >> x;

	cout << binarySearch(input, n, x) << endl; 	

}
```

###  Selection Sort
![image](https://user-images.githubusercontent.com/57065763/187026886-62f1723e-abce-48d7-9ea5-628faf3653d3.png)

 

```cpp
 

/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;

void selectionSort(int input[], int n) {
	for(int i = 0; i < n-1; i++ ) {
	// Find min element in the array
	int min = input[i], minIndex = i;
	for(int j = i+1; j < n; j++) {
		if(input[j] < min) {
			min = input[j];
			minIndex = j;
		}
	}
	// Swap
	int temp = input[i];
	input[i] = input[minIndex];
	input[minIndex] = temp;
	}
}

int main() {
	int input[] = {3, 1, 6, 9, 0, 4};
	selectionSort(input, 6);
	for(int i = 0; i < 6; i++) {
		cout << input[i] << " ";
			 
	}
	cout << endl;
}

```

###  Understanding Bubble Sort
![image](https://user-images.githubusercontent.com/57065763/187026935-541cd282-f307-414e-9316-a5b728188c80.png)

###  Code Bubble Sort

```
Code Bubble Sort
 
Provided with a random integer array/list(ARR) of size N, you have been required to sort this array using 'Bubble Sort'.
Note:
Change in the input array/list itself. You don't need to return or print the elements.
Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains an integer 'N' representing the size of the array/list.

Second line contains 'N' single space separated integers representing the elements in the array/list.
Output format :
For each test case, print the elements of the array/list in sorted order separated by a single space.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^3
Time Limit: 1 sec
Sample Input 1:
1
7
2 13 4 1 3 6 28
Sample Output 1:
1 2 3 4 6 13 28
Sample Input 2:
2
5
9 3 6 2 0
4
4 3 2 1
Sample Output 2:
0 2 3 6 9
1 2 3 4
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{

	int t;
	cin >> t;

	while (t--)
	{
		int size;
		cin >> size;

		int *input = new int[size];

		for (int i = 0; i < size; ++i)
		{
			cin >> input[i];
		}

		bubbleSort(input, size);

		for (int i = 0; i < size; ++i)
		{
			cout << input[i] << " ";
		}

		delete[] input;
		cout << endl;
	}
}
*/

/*-------------------------------CODE------------------------*/
void bubbleSort(int *input, int size) { 
    for (int i = 0; i < size - 1; i++) { 
        for (int j = 0; j < size - i - 1; j++) { 
            if (input[j] > input[j + 1]) { 
                int tmp = input[j]; 
                input[j] = input[j + 1]; 
                input[j + 1] = tmp; 
            } 
        } 
    } 
}
```

###  Bubble Sort
![image](https://user-images.githubusercontent.com/57065763/187027123-9b419d12-b0a5-4746-8a8d-043fd54615fc.png)

###  Understanding Insertion Sort

![image](https://user-images.githubusercontent.com/57065763/187027276-686c9994-62b3-480b-ac5a-5d05c3f237c9.png)

###  Code Insertion Sort

```
Code Insertion Sort
 
Provided with a random integer array/list(ARR) of size N, you have been required to sort this array using 'Insertion Sort'.
 Note:
Change in the input array/list itself. You don't need to return or print the elements.
 Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains an integer 'N' representing the size of the array/list.

Second line contains 'N' single space separated integers representing the elements in the array/list.
Output Format :
For each test case, print the elements of the array/list in sorted order separated by a single space.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^3
Time Limit: 1 sec
Sample Input 1:
1
7
2 13 4 1 3 6 28
Sample Output 1:
1 2 3 4 6 13 28
Sample Input 2:
2
5
9 3 6 2 0
4
4 3 2 1
Sample Output 2:
0 2 3 6 9
1 2 3 4 
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{
	int t;
	cin >> t;
	
	while (t--)
	{
		int size;
		cin >> size;
		int *input = new int[size];

		for (int i = 0; i < size; i++)
		{
			cin >> input[i];
		}

		insertionSort(input, size);

		for (int i = 0; i < size; i++)
		{
			cout << input[i] << " ";
		}

		delete[] input;
		cout << endl;
	}

	return 0;
}
*/

/*-------------------------------CODE------------------------*/
void insertionSort(int *input, int size)
{
    for(int i=1; i<size; i++){
        int current = input[i];
        int j;
        for(j=i-1; j>=0; j--){
            if(current <input[j]){
                input[j+1]= input[j];
            }else{
                break;
            }
        }
    	input[j+1] = current;
    }
}
```

###  Insertion Sort

```cpp
 

/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;

void insertionSort(int arr[], int n) {
	for(int i = 1; i < n; i++) {
		int current = arr[i];
		int j;
		for(j = i - 1; j >= 0; j--) {
			if(current < arr[j]) {
				arr[j+1] = arr[j];
			}
			else {
				break;
			}
		}
		arr[j+1] = current;
	}

}

void printArray(int input[], int n) {
	for(int i = 0; i < n; i++) {
		cout << input[i] << " " ;
	}
	cout << endl;
}

int main() {
	// Take array input from the user
	int n;
	cin >> n;

	int input[100];
	
	for(int i = 0; i < n; i++) {
		cin >> input[i];
	}
	
	insertionSort(input, n);

	printArray(input, n);
	
}

```

###   How to Merge two sorted arrays ? 
![image](https://user-images.githubusercontent.com/57065763/187028328-38ea7738-9d5e-44fe-b251-bdff01d54dd5.png)

###  Code Merge Two Sorted Arrays

```
Code Merge Two Sorted Arrays
 
You have been given two sorted arrays/lists(ARR1 and ARR2) of size N and M respectively, merge them into a third array/list such that the third array is also sorted.
Input Format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains an integer 'N' representing the size of the first array/list.

Second line contains 'N' single space separated integers representing the elements of the first array/list.

Third line contains an integer 'M' representing the size of the second array/list.

Fourth line contains 'M' single space separated integers representing the elements of the second array/list.
Output Format :
For each test case, print the sorted array/list(of size N + M) in a single row, separated by a single space.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^5
0 <= M <= 10^5
Time Limit: 1 sec 
Sample Input 1 :
1
5
1 3 4 7 11
4
2 4 6 13
Sample Output 1 :
1 2 3 4 4 6 7 11 13 
Sample Input 2 :
2
3
10 100 500
7
4 7 9 25 30 300 450
4
7 45 89 90
0
Sample Output 2 :
4 7 9 10 25 30 100 300 450 500
7 45 89 90
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{
	int t;
	cin >> t;
	
	while (t--)
	{
		int size1;
		cin >> size1;

		int *arr1 = new int[size1];

		for (int i = 0; i < size1; i++)
		{
			cin >> arr1[i];
		}

		int size2;
		cin >> size2;

		int *arr2 = new int[size2];

		for (int i = 0; i < size2; i++)
		{
			cin >> arr2[i];
		}

		int *ans = new int[size1 + size2];

		merge(arr1, size1, arr2, size2, ans);

		for (int i = 0; i < size1 + size2; i++)
		{
			cout << ans[i] << " ";
		}

		cout << endl;
		delete[] arr1;
		delete[] arr2;
		delete[] ans;
	}
}
*/

/*-------------------------------CODE------------------------*/
void merge(int *arr1, int size1, int *arr2, int size2, int *ans)
{
    int i=0, j=0,k=0;
    
    while(i<size1 && j<size2){
        if(arr1[i]<=arr2[j]){
            ans[k++]=arr1[i++];
        }else{
            ans[k++]=arr2[j++];
        }
    }
    while(i<size1){
        ans[k++]=arr1[i++];
    }
    while(j<size2){
        ans[k++]=arr2[j++];
    }
}

```

###  Push Zeros to end

```
Push Zeros to end
 
You have been given a random integer array/list(ARR) of size N. You have been required to push all the zeros that are present in the array/list to the end of it. Also, make sure to maintain the relative order of the non-zero elements.
Note:
Change in the input array/list itself. You don't need to return or print the elements.

You need to do this in one scan of array only. Don't use extra space.


Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains an integer 'N' representing the size of the array/list.

Second line contains 'N' single space separated integers representing the elements in the array/list.
Output Format :
For each test case, print the elements of the array/list in the desired order separated by a single space.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^5
Time Limit: 1 sec
Sample Input 1:
1
7
2 0 0 1 3 0 0
Sample Output 1:
2 1 3 0 0 0 0
 Explanation for the Sample Input 1 :
All the zeros have been pushed towards the end of the array/list. Another important fact is that the order of the non-zero elements have been maintained as they appear in the input array/list.
Sample Input 2:
2
5
0 3 0 2 0
5
9 0 0 8 2
Sample Output 2:
3 2 0 0 0
9 8 2 0 0 
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{

	int t;
	cin >> t;
	
	while (t--)
	{

		int size;

		cin >> size;
		int *input = new int[size];

		for (int i = 0; i < size; i++)
		{
			cin >> input[i];
		}

		pushZeroesEnd(input, size);

		for (int i = 0; i < size; i++)
		{
			cout << input[i] << " ";
		}

		cout << endl;
		delete[] input;
	}

	return 0;
}
*/

/*-------------------------------CODE------------------------*/
void pushZeroesEnd(int *input, int size)
{
    //SWAP WAY
    int count = 0;
    for(int i=0; i<size; ++i){
        if(input[i]!=0){
            swap(input[i], input[count]); 
            count++;
        }
    }
}
```

###  Rotate array

```
Rotate array
 
You have been given a random integer array/list(ARR) of size N. Write a function that rotates the given array/list by D elements(towards the left).
 Note:
Change in the input array/list itself. You don't need to return or print the elements.
Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains an integer 'N' representing the size of the array/list.

Second line contains 'N' single space separated integers representing the elements in the array/list.

Third line contains the value of 'D' by which the array/list needs to be rotated.
Output Format :
For each test case, print the rotated array/list in a row separated by a single space.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^4
0 <= N <= 10^6
0 <= D <= N
Time Limit: 1 sec
Sample Input 1:
1
7
1 2 3 4 5 6 7
2
Sample Output 1:
3 4 5 6 7 1 2
Sample Input 2:
2
7
1 2 3 4 5 6 7
0
4
1 2 3 4
2
Sample Output 2:
1 2 3 4 5 6 7
3 4 1 2
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{
	int t;
	cin >> t;
	
	while (t--)
	{
		int size;
		cin >> size;

		int *input = new int[size];

		for (int i = 0; i < size; ++i)
		{
			cin >> input[i];
		}

		int d;
		cin >> d;

		rotate(input, d, size);

		for (int i = 0; i < size; ++i)
		{
			cout << input[i] << " ";
		}
		
		delete[] input;
		cout << endl;
	}

	return 0;
}
*/

/*-------------------------------CODE------------------------*/
//2nd APPROACH
void reverse(int *input, int i, int j){
    while(i<j){
        swap(input[i],input[j]);
        i++;
        j--;
    }
}

void rotate(int *input, int d, int n)
{
    reverse(input, 0,n-1);
    reverse(input, 0,n-d-1);
    reverse(input, n-d,n-1);
}


/*
// //FIRST  APPROACH
void rotate(int *input, int d, int n)
{
    int arr[d];
    for(int i=0; i<d; i++){
        arr[i]=input[i];
    }
    int j=0;
    for(int i=d; i<n; i++){
        input[j]=input[i];
        j++;
    }
    for(int i=0; i<d; i++){
        input[j]=arr[i];
        j++;
    }
}
*/
```

###  Second Largest in array

```
Second Largest in array
 
You have been given a random integer array/list(ARR) of size N. You are required to find and return the second largest element present in the array/list.
If N <= 1 or all the elements are same in the array/list then return -2147483648 or -2 ^ 31(It is the smallest value for the range of Integer)
Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

The first line of each test case or query contains an integer 'N' representing the size of the array/list.

The second line contains 'N' single space separated integers representing the elements in the array/list.
Output Format :
For each test case, print the second largest in the array/list if exists, -2147483648 otherwise.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^5

Time Limit: 1 sec
Sample Input 1:
1
7
2 13 4 1 3 6 28
Sample Output 1:
13
Sample Input 2:
1
5
9 3 6 2 9
Sample Output 2:
6
Sample Input 3:
2
2
6 6
4
90 8 90 5
Sample Output 3:
-2147483648
8
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{
	int t;
	cin >> t;
	while (t--)
	{

		int size;
		cin >> size;
		int *input = new int[size];

		for (int i = 0; i < size; i++)
		{
			cin >> input[i];
		}

		cout << findSecondLargest(input, size) << endl;

		delete[] input;
	}

	return 0;
}
*/

/*-------------------------------CODE------------------------*/
#include<climits>
int findSecondLargest(int *input, int n)
{
    //Write your code here
    if (n <= 0) {
        return INT_MIN;
    }
    int largest=input[0];
    int second_largest=INT_MIN;
    for(int i=0;i<n;i++){
        if(input[i]>largest){
            second_largest=largest;
            largest=input[i];
        }
        else if(second_largest<input[i] && input[i]<largest ){
            second_largest=input[i];
        }
        
    }
    return second_largest;
}
```

###  Check Array Rotation

```
Check Array Rotation
 
You have been given an integer array/list(ARR) of size N. It has been sorted(in increasing order) and then rotated by some number 'K' in the right hand direction.
Your task is to write a function that returns the value of 'K', that means, the index from which the array/list has been rotated.
Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains an integer 'N' representing the size of the array/list.

Second line contains 'N' single space separated integers representing the elements in the array/list.
Output Format :
For each test case, print the value of 'K' or the index from which which the array/list has been rotated.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^5
Time Limit: 1 sec
Sample Input 1:
1
6
5 6 1 2 3 4
Sample Output 1:
2
Sample Input 2:
2
5
3 6 8 9 10
4
10 20 30 1
Sample Output 2:
0
3
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{

	int t;
	cin >> t;
	while (t--)
	{

		int size;
		cin >> size;
		int *input = new int[size];

		for (int i = 0; i < size; i++)
		{
			cin >> input[i];
		}

		cout << arrayRotateCheck(input, size) << endl;
		delete[] input;
	}
	
	return 0;
}
*/

/*-------------------------------CODE------------------------*/
int arrayRotateCheck(int *input, int size) { 
    for(int i=0; i<size-1; i++){
        if(input[i]>input[i+1]){
            return i+1;
        }
    }
    return 0;
}
```

###  Sort 0 1 2

```
Sort 0 1 2
 
You are given an integer array/list(ARR) of size N. It contains only 0s, 1s and 2s. Write a solution to sort this array/list in a 'single scan'.
'Single Scan' refers to iterating over the array/list just once or to put it in other words, you will be visiting each element in the array/list just once.
Note:
You need to change in the given array/list itself. Hence, no need to return or print anything. 
Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains an integer 'N' representing the size of the array/list.

Second line contains 'N' single space separated integers(all 0s, 1s and 2s) representing the elements in the array/list.
Output Format :
For each test case, print the sorted array/list elements in a row separated by a single space.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^5
Time Limit: 1 sec
Sample Input 1:
1
7
0 1 2 0 2 0 1
Sample Output 1:
0 0 0 1 1 2 2 
Sample Input 2:
2
5
2 2 0 1 1
7
0 1 2 0 1 2 0
Sample Output 2:
0 1 1 2 2 
0 0 0 1 1 2 2
```

```cpp
/*
#include <iostream>
#include <algorithm>
using namespace std;

#include "solution.h"

int main()
{
	int t;
	cin >> t;
	while (t--)
	{
		int size;

		cin >> size;
		int *arr = new int[size];

		for (int i = 0; i < size; i++)
		{
			cin >> arr[i];
		}

		sort012(arr, size);

		for (int i = 0; i < size; i++)
		{
			cout << arr[i] << " ";
		}

		delete[] arr;
		cout << endl;
	}

	return 0;
}
*/

/*-------------------------------CODE------------------------*/
void sort012(int *arr, int n) { 
    int i = 0; 
    int nextZero = 0; 
    int nextTwo = n - 1; 
    
    while (i <= nextTwo) { 
        if (arr[i] == 0) { 
/* You can replace the next three lines with CPP's inbuilt swap function. swap(arr[i], arr[nextZero]) will swap the values of arr[i] and arr[nextZero]. */ 
            // int temp = arr[i]; 
            // arr[i] = arr[nextZero]; 
            // arr[nextZero] = temp; 
            swap(arr[i], arr[nextZero]);
            i++; 
            nextZero++; 
        } else if (arr[i] == 2) { 
            // int temp = arr[i]; 
            // arr[i] = arr[nextTwo]; 
            // arr[nextTwo] = temp;
            swap(arr[i], arr[nextTwo]);
            nextTwo--; 
        } else { 
            i++; 
        } 
    } 
}
```

###  Sum of Two Arrays

```
Sum of Two Arrays
 
Two random integer arrays/lists have been given as ARR1 and ARR2 of size N and M respectively. Both the arrays/lists contain numbers from 0 to 9(i.e. single digit integer is present at every index). The idea here is to represent each array/list as an integer in itself of digits N and M.
You need to find the sum of both the input arrays/list treating them as two integers and put the result in another array/list i.e. output array/list will also contain only single digit at every index.
Note:
The sizes N and M can be different. 

Output array/list(of all 0s) has been provided as a function argument. Its size will always be one more than the size of the bigger array/list. Place 0 at the 0th index if there is no carry. 

No need to print the elements of the output array/list.
Using the function "sumOfTwoArrays", write the solution to the problem and store the answer inside this output array/list. The main code will handle the printing of the output on its own.
Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains an integer 'N' representing the size of the first array/list.

Second line contains 'N' single space separated integers representing the elements of the first array/list.

Third line contains an integer 'M' representing the size of the second array/list.

Fourth line contains 'M' single space separated integers representing the elements of the second array/list.
Output Format :
For each test case, print the required sum of the arrays/list in a row, separated by a single space.

Output for every test case will be printed in a separate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^5
0 <= M <= 10^5
Time Limit: 1 sec 
Sample Input 1:
1
3
6 2 4
3
7 5 6
Sample Output 1:
1 3 8 0
Sample Input 2:
2
3
8 5 2
2
1 3
4
9 7 6 1
3
4 5 9
Sample Output 2:
0 8 6 5
1 0 2 2 0 
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{
	int t;
	cin >> t;

	while (t--)
	{
		int size1;
		cin >> size1;

		int *input1 = new int[size1];

		for (int i = 0; i < size1; ++i)
		{
			cin >> input1[i];
		}

		int size2;
		cin >> size2;

		int *input2 = new int[size2];

		for (int i = 0; i < size2; ++i)
		{
			cin >> input2[i];
		}

		int outsize = 1 + max(size1, size2);

		int *output = new int[outsize];

		sumOfTwoArrays(input1, size1, input2, size2, output);

		for (int i = 0; i < outsize; ++i)
		{
			cout << output[i] << " ";
		}

		delete[] input1;
		delete[] input2;
		delete[] output;
		cout << endl;
	}

	return 0;
}
*/

/*-------------------------------CODE------------------------*/
void sumOfTwoArrays(int *input1, int size1, int *input2, int size2, int *output)
{
    int i = size1-1, j=size2-1, k=max(size1,size2), carry=0, total,reminder;
    
    while(i>=0 && j>=0){
        total = input1[i--]+input2[j--]+carry;
        reminder = total%10;
        carry = total/10;
        output[k--] = reminder;
    }

    while(i>=0){
        total = input1[i--] + carry;
        reminder = total%10;
        carry = total/10;
        output[k--] = reminder;
    }
    
    while(j>=0){
        total = input2[j--] + carry;
        reminder = total%10;
        carry = total/10;
        output[k--] = reminder;
    }
    output[k--] = carry; 
}
```

```

Lecture 9: Searching and Sorting END HERE

```

```

Lecture 10: Character Arrays and 2D Arrays START HERE

```

# ##Lecture 10: Character Arrays and 2D Arrays

---

//============>>>>>>>>>> Lecture 10: Character Arrays and 2D Arrays Notes
[Lecture 10: Character Arrays and 2D Arrays Notes.pdf](https://github.com/karakib2k18/Cpp-Programming-Language-For-DSA/files/9432228/Lecture.10.Character.Arrays.and.2D.Arrays.Notes.pdf)

---

### Character Arrays
![image](https://user-images.githubusercontent.com/57065763/186830470-a92dc2e2-eb7c-4211-89c4-def9ae4c8de1.png)

```cpp
#include <iostream>
using namespace std;

int length(char input[]) {
	int count = 0;
	for(int i = 0; input[i] != '\0'; i++) {
		count++;
	}
	return count;
}

int main() {
	char name[100];
	cout << "Enter your name : ";
	cin >> name;
	/*
	name[4] = 'x';
	name[3] = 'd';
	name[1] = '\0';
	*/
	cout << "Name : " << name << endl;
	cout << "Length : " << length(name) << endl;
}
```

### Check Palindrome

```
Check Palindrome
 
Given a string, determine if it is a palindrome, considering only alphanumeric characters.
Palindrome
A palindrome is a word, number, phrase, or other sequences of characters which read the same backwards and forwards.
Example:
If the input string happens to be, "malayalam" then as we see that this word can be read the same as forward and backwards, it is said to be a valid palindrome.

The expected output for this example will print, 'true'.
From that being said, you are required to return a boolean value from the function that has been asked to implement.
Input Format:
The first and only line of input contains a string without any leading and trailing spaces. All the characters in the string would be in lower case.
Output Format:
The only line of output prints either 'true' or 'false'.
Note:
You are not required to print anything. It has already been taken care of.
Constraints:
0 <= N <= 10^6
Where N is the length of the input string.

Time Limit: 1 second
Sample Input 1 :
abcdcba
Sample Output 1 :
true 
Sample Input 2:
coding
Sample Output 2:
false
```

```cpp
/*
#include <iostream>
#include <cstring>
using namespace std;

#include "solution.h"

int main() {
    int size = 1e6;
    char str[size];
    cin >> str;
    cout << (checkPalindrome(str) ? "true" : "false");
}
*/

/*-------------------------------CODE------------------------*/
/*Time complexity: O(N) Space complexity: O(1) where N is the length of the input string */
int length(char str[])
{
	int count = 0;
	for (int i = 0; str[i] != '\0'; i++)
	{
		count++;
	}
	return count;
}
bool checkPalindrome(char str[])
{
	for (int i = 0; i <= length(str) / 2; i++)
	{
		if (str[i] != str[length(str) - 1 - i])
		{
			return false;
		}
	}
	return true;
}
```

### Replace Character

```
Replace Character
 
Given an input string S and two characters c1 and c2, you need to replace every occurrence of character c1 with character c2 in the given string.
Input Format :
Line 1 : Input String S
Line 2 : Character c1 and c2 (separated by space)
Output Format :
Updated string
Note :
You don't need to output anything. Just implement the given function.
Constraints :
1 <= Length of String S <= 10^6
Sample Input :
abacd
a x
Sample Output :
xbxcd
```

```cpp
/*
#include <iostream>
#include <cstring>
using namespace std;

#include "solution.h"

int main() {
    char input[1000000];
    char c1, c2;
    cin >> input;
    cin >> c1 >> c2;
    replaceCharacter(input, c1, c2);
    cout << input << endl;
}
*/

/*-------------------------------CODE------------------------*/
/*Time complexity: O(N) Space complexity: O(1) where N is the length of the input string */
void replaceCharacter(char input[], char c1, char c2)
{
// ---------------FIRST APPROACH----------------
	for (int i = 0; input[i] != '\0'; i++)
	{
		if (input[i] == c1)
		{
			input[i] = c2;
		}
	}
    
// --------------SECOND APPROACH--------------
    int length = strlen(input);
    for(int i=0; i<length; ++i){
        if(input[i]==c1){
            input[i]=c2;
        }
    }
}
```


### More on Character Arrays
![image](https://user-images.githubusercontent.com/57065763/186832905-c6b4b169-1a36-4883-a885-405784477eaf.png)

```cpp
#include <iostream>
using namespace std;

int length(char input[]) {
	int count = 0;
	for(int i = 0; input[i] != '\0'; i++) {
		count++;
	}
	return count;
}

void reverseString(char input[]) {
	int len = length(input);
	int i = 0, j = len - 1;
	while(i < j) {
		char temp = input[i];
		input[i] = input[j];
		input[j] = temp;
		i++;
		j--;
	}
}

int main() {
	char input[100];
	//cin >> input;
	cin.getline(input, 100);
	
	reverseString(input);
	cout << input << endl;
}
```


### Trim Spaces

```
Trim Spaces
 
Given an input string S that contains multiple words, you need to remove all the spaces present in the input string.
There can be multiple spaces present after any word.
Input Format :
 String S
Output Format :
Updated string
Constraints :
1 <= Length of string S <= 10^6
Sample Input :
abc def g hi
Sample Output :
abcdefghi
```

```cpp
/*
#include <iostream>
#include <cstring>
using namespace std;

#include "solution.h"

int main() {
    char input[1000000];
    cin.getline(input, 1000000);
    trimSpaces(input);
    cout << input << endl;
}
*/

/*-------------------------------CODE------------------------*/
/*Time complexity: O(N) Space complexity: O(1) where N is the length of the input string */
void trimSpaces(char input[])
{
	int j = 0;
	for (int i = 0; input[i] != '\0'; i++)
	{
		if (input[i] != ' ')
		{
			input[j] = input[i];
			j++;
		}
	}
	input[j] = '\0';
}
```

### Reverse Word Wise

```
Reverse Word Wise
 
Reverse the given string word wise. That is, the last word in given string should come at 1st place, last second word at 2nd place and so on. Individual words should remain as it is.
Input format :
String in a single line
Output format :
Word wise reversed string in a single line
Constraints :
0 <= |S| <= 10^7
where |S| represents the length of string, S.
Sample Input 1:
Welcome to Coding Ninjas
Sample Output 1:
Ninjas Coding to Welcome
Sample Input 2:
Always indent your code
Sample Output 2:
code your indent Always
```

```cpp
/*
#include <iostream>
#include "solution.h"
using namespace std;

int main() {
    char input[1000];
    cin.getline(input, 1000);
    reverseStringWordWise(input);
    cout << input << endl;
}
*/

/*-------------------------------CODE------------------------*/
//-----------------------NORMAL WAY-------------------------
#include <cstring>
using namespace std;
void reverseStringWordWise(char input[]) {
    
    int i=0;
    int j=strlen(input)-1;
    int size = strlen(input);
    
    while(i<j){
        swap(input[i], input[j]);
        i++;
        j--;
        
    }

    i=0;
    int start =0;
    while(i<=size){
        if(input[i]==' ' || input[i]=='\0'){
            int end=i-1;
            while(start<=end)
            {
            	swap(input[start],input[end]);
            	start++;
            	end--;
            }
            start = i+1;
        }
        i++;
    }  
    
}

//--------------------CN WAY--------------------------
/*Time Complexity : O(n) Space Complexity : O(1) where n is size of input array */
using namespace std;
void reverse(char input[], int start, int end)
{
	while (start < end)
	{
		swap(input[start++], input[end--]);
	}
}
void reverseStringWordWise(char input[])
{
	int previousSpaceIndex = -1;
	int i = 0;
	for (; input[i] != '\0'; i++)
	{
		if (input[i] == ' ')
		{
			reverse(input, previousSpaceIndex + 1, i - 1);
			previousSpaceIndex = i;
		}
	}
	reverse(input, previousSpaceIndex + 1, i - 1);
	reverse(input, 0, i - 1);
}
```

### Inbuilt Functions
![image](https://user-images.githubusercontent.com/57065763/186837227-0f84a644-0640-4b54-9835-7edbddba4ac8.png)

```cpp
#include <iostream>
using namespace std;
#include <cstring>


void printAllPrefixes(char input[]) {
	// i represents end index of my prefix
	for(int i = 0; input[i] != '\0'; i++) {
			// j represents start index of my prefix
		for(int j = 0; j <= i; j++) {
			cout << input[j];
		}
		cout << endl;
	}
}

int main() {
	char input1[100] = "abcd";
	printAllPrefixes(input1);

	/*
	char input2[100] = "xy";
	cout << "Before copying : ";
	cout << "Input 1 : " << input1 << endl;
	cout << "Input 2 : " << input2 << endl;
	//strcpy(input1, "hello");
	strncpy(input1, input2, 4);
	
	cout << "After copying : ";
	cout << "Input 1 : " << input1 << endl;
	cout << "Input 2 : " << input2 << endl;
	*/

	//cin >> input1;
	//cin >> input2;

	/*
	if(strcmp(input1, input2) == 0) {
		cout << "true" << endl;
	}
	else {
		cout << "false" << endl;
	}
	*/

	/*
	int len = strlen(input);
	cout << "Length : " << len << endl;
	*/
}
```

### Print All Substrings

```
Print All Substrings
 
For a given input string(str), write a function to print all the possible substrings.
Substring
A substring is a contiguous sequence of characters within a string. 
Example: "cod" is a substring of "coding". Whereas, "cdng" is not as the characters taken are not contiguous
Input Format:
The first and only line of input contains a string without any leading and trailing spaces. All the characters in the string would be in lower case.
Output Format:
Print the total number of substrings possible, where every substring is printed on a single line and hence the total number of output lines will be equal to the total number of substrings.
Note:
The order in which the substrings are printed, does not matter.
Constraints:
0 <= N <= 10^6
Where N is the length of the input string.

Time Limit: 1 second
Sample Input 1:
abc
Sample Output 1:
a 
ab 
abc 
b 
bc 
c 
 Sample Input 2:
co
Sample Output 2:
c 
co 
o
```

```cpp
/*
#include <iostream>
#include <cstring>
using namespace std;

#include "solution.h"

int main() {
    int size = 1e6;
    char str[size];
    cin >> str;
    printSubstrings(str);
}
*/

/*-------------------------------CODE------------------------*/
/*Time complexity: O(N^3) Space complexity: O(1) where N is the length of the input string */
void printSubstrings(char input[])
{
	int k = 1;
	while (k <= strlen(input))
	{
		for (int i = 0; i <= strlen(input) - k; i++)
		{
			for (int j = i; j < i + k; j++)
			{
				cout << input[j];
			}
			cout << endl;
		}
		k++;
	}
}
```

### 2D Arrays
![image](https://user-images.githubusercontent.com/57065763/186839201-b4f24f6e-461f-4b54-b4ea-fd510acb7c69.png)

```cpp
#include <iostream>
using namespace std;

int main() {
	int a[100][100];
	int m, n;
	cin >> m >> n;


	// Taking input
	for(int i = 0; i < m; i++) {
		for(int j = 0; j < n; j++) {
			cin >> a[i][j];
		}
	}

	// print array row wise
	cout << "Row wise : " << endl;
	for(int i = 0; i < m; i++) {
		for(int j = 0;  j < n; j++) {
			cout << a[i][j] << " ";
		}
		cout << endl;	
	}

	cout << "Column wise : " << endl;
	for(int j = 0; j < n; j++) {
		for(int i = 0; i < m; i++) {
			cout << a[i][j] << " ";
		}
		cout << endl;
	}
}
```


### Column Wise Sum

```
Column Wise Sum
 
Given a 2D integer array of size M*N, find and print the sum of ith column elements separated by space.
Input Format :
First and only line of input contains M and N, followed by M * N space separated integers representing the elements in the 2D array.
Output Format :
Sum of every ith column elements (separated by space)
Constraints :
1 <= M, N <= 10^3
Sample Input :
4 2 1 2 3 4 5 6 7 8
Sample Output :
16 20
```

```cpp
/*-------------------------------CODE------------------------*/
#include<iostream>
using namespace std;


int main(){

  int m,n;
    cin>>m>>n;
    int arr[m][n];
    for(int i=0; i<m; ++i){
        for(int j=0; j<n; ++j){
            cin>>arr[i][j];
        }    
    }
    
    for(int j=0; j<n; ++j){
        int sum=0;
        for(int i=0; i<m; ++i){
            sum = sum + arr[i][j];
        }
        cout << sum << " ";
    }
}
```

### How are 2D Arrays Stored ?
![image](https://user-images.githubusercontent.com/57065763/186869717-00ccb777-806d-4fb0-9eee-fd14a1833676.png)

```cpp
#include <iostream>
using namespace std;

void printArray(int a[][5], int m, int n) {
	for(int i = 0; i < m; i++) {
		for(int j = 0;  j < n; j++) {
			cout << a[i][j] << " ";
		}
		cout << endl;	
	}
}

int main() {

	int a[5][5] = {{1, 2}, {3, 4}};
	printArray(a, 5, 5);


	/*
	int a[100][100];
	int m, n;
	cin >> m >> n;


	// Taking input
	for(int i = 0; i < m; i++) {
		for(int j = 0; j < n; j++) {
			cin >> a[i][j];
		}
	}

	printArray(a, m, n);
	*/
	/*
	// print array row wise
	cout << "Row wise : " << endl;
	for(int i = 0; i < m; i++) {
		for(int j = 0;  j < n; j++) {
			cout << a[i][j] << " ";
		}
		cout << endl;	
	}

	cout << "Column wise : " << endl;
	for(int j = 0; j < n; j++) {
		for(int i = 0; i < m; i++) {
			cout << a[i][j] << " ";
		}
		cout << endl;
	}
	*/
}
```

### Largest Row or Column

```
Largest Row or Column
 
For a given two-dimensional integer array/list of size (N x M), you need to find out which row or column has the largest sum(sum of all the elements in a row/column) amongst all the rows and columns.
Note :
If there are more than one rows/columns with maximum sum, consider the row/column that comes first. And if ith row and jth column has the same largest sum, consider the ith row as answer.
Input Format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains two integer values, 'N' and 'M', separated by a single space. They represent the 'rows' and 'columns' respectively, for the two-dimensional array/list.

Second line onwards, the next 'N' lines or rows represent the ith row values.

Each of the ith row constitutes 'M' column values separated by a single space.
Output Format :
For each test case, If row sum is maximum, then print: "row" <row_index> <row_sum>
OR
If column sum is maximum, then print: "column" <col_index> <col_sum>
It will be printed in a single line separated by a single space between each piece of information.

Output for every test case will be printed in a seperate line.
 Consider :
If there doesn't exist a sum at all then print "row 0 -2147483648", where -2147483648 or -2^31 is the smallest value for the range of Integer.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^3
0 <= M <= 10^3
Time Limit: 1sec
Sample Input 1 :
1
2 2 
1 1 
1 1
Sample Output 1 :
row 0 2
Sample Input 2 :
2
3 3
3 6 9 
1 4 7 
2 8 9
4 2
1 2
90 100
3 40
-10 200
Sample Output 2 :
column 2 25
column 1 342
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{
	int t;
	cin >> t;
	while (t--)
	{
		int row, col;
		cin >> row >> col;

		int **input = new int *[row];
		for (int i = 0; i < row; i++)
		{
			input[i] = new int[col];
			for (int j = 0; j < col; j++)
			{
				cin >> input[i][j];
			}
		}

		findLargest(input, row, col);
		cout << endl;
	}
}
*/

/*-------------------------------CODE------------------------*/
#include <climits> 

void findLargest(int **input, int nRows, int mCols) { 
    bool isRow = true; 
    int largestSum = INT_MIN; 
    int num = 0; 
    for (int i = 0; i < nRows; i++) { 
        int rowSum = 0; 
        for (int j = 0; j < mCols; j++) { 
            rowSum += input[i][j]; 
        } 
        
        if (rowSum > largestSum) { 
            largestSum = rowSum; 
            num = i; 
        } 
    } 
    
    for (int j = 0; j < mCols; j++) { 
        int colSum = 0; 
        for (int i = 0; i < nRows; i++) { 
            colSum += input[i][j]; 
        } 
        
        if (colSum > largestSum) { 
            largestSum = colSum; 
            num = j; 
            isRow = false; 
        } 
    } 
    
    if (isRow) { 
        cout << "row" << " " << num << " " << largestSum; 
    } else { 
        cout << "column" << " " << num << " " << largestSum; 
    } 
}
```


### Wave Print

```
Wave Print
 
For a given two-dimensional integer array/list of size (N x M), print the array/list in a sine wave order, i.e, print the first column top to bottom, next column bottom to top and so on.
Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains two integer values, 'N' and 'M', separated by a single space. They represent the 'rows' and 'columns' respectively, for the two-dimensional array/list.

Second line onwards, the next 'N' lines or rows represent the ith row values.

Each of the ith row constitutes 'M' column values separated by a single space.
Output format :
For each test case, print the elements of the two-dimensional array/list in the sine wave order in a single line, separated by a single space.

Output for every test case will be printed in a seperate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^3
0 <= M <= 10^3
Time Limit: 1sec
Sample Input 1:
1
3 4 
1  2  3  4 
5  6  7  8 
9 10 11 12
Sample Output 1:
1 5 9 10 6 2 3 7 11 12 8 4
Sample Input 2:
2
5 3 
1 2 3 
4 5 6 
7 8 9 
10 11 12 
13 14 15
3 3
10 20 30 
40 50 60
70 80 90
Sample Output 2:
1 4 7 10 13 14 11 8 5 2 3 6 9 12 15 
10 40 70 80 50 20 30 60 90 
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{
	int t;
	cin >> t;
	while (t--)
	{
		int row, col;
		cin >> row >> col;
		int **input = new int *[row];
		for (int i = 0; i < row; i++)
		{
			input[i] = new int[col];
			for (int j = 0; j < col; j++)
			{
				cin >> input[i][j];
			}
		}
		wavePrint(input, row, col);
		cout << endl;
	}
}
*/

/*-------------------------------CODE------------------------*/
void wavePrint(int **input, int nRows, int mCols)
{
    
/*
00
10
20

21
11
01

02
12
22
*/
 
//     // FIRST AND MY APPRAOCH
    
//     if (nRows == 0) { return; }
    
//     int top_down = 0;
//     for(int i=0; i< mCols; i++){
//         if(top_down>0){
//             for(int j=nRows-1; j>=0; j--){
//                 cout<< input[j][i]<<" ";
//                 top_down--;
//             }    
//         }else{
//             for(int j=0; j<nRows; j++){
//                 cout<< input[j][i]<<" ";
//                 top_down++;
//             }
//         }
//     }
    
    //SECOND AND SOLUTIN APPROACH
    
    if (nRows == 0) { return; }

    for(int i=0; i< mCols; i++){
        if (i % 2 == 0){
            for(int j=0; j<nRows; j++){
            	cout<< input[j][i]<<" ";
            }  
        }else{
            for(int j=nRows-1; j>=0; j--){
            	cout<< input[j][i]<<" ";
            }    
        }
    }
}
```


### Spiral Print
![image](https://user-images.githubusercontent.com/57065763/186873071-360b88a7-c18f-47dd-9536-f574f65f99de.png)

```
Spiral Print
 
For a given two-dimensional integer array/list of size (N x M), print it in a spiral form. That is, you need to print in the order followed for every iteration:
a. First row(left to right)
b. Last column(top to bottom)
c. Last row(right to left)
d. First column(bottom to top)
 Mind that every element will be printed only once.
Refer to the Image:
Spiral path of a matrix

Input format :
The first line contains an Integer 't' which denotes the number of test cases or queries to be run. Then the test cases follow.

First line of each test case or query contains two integer values, 'N' and 'M', separated by a single space. They represent the 'rows' and 'columns' respectively, for the two-dimensional array/list.

Second line onwards, the next 'N' lines or rows represent the ith row values.

Each of the ith row constitutes 'M' column values separated by a single space.
Output format :
For each test case, print the elements of the two-dimensional array/list in the spiral form in a single line, separated by a single space.

Output for every test case will be printed in a seperate line.
Constraints :
1 <= t <= 10^2
0 <= N <= 10^3
0 <= M <= 10^3
Time Limit: 1sec
Sample Input 1:
1
4 4 
1 2 3 4 
5 6 7 8 
9 10 11 12 
13 14 15 16
Sample Output 1:
1 2 3 4 8 12 16 15 14 13 9 5 6 7 11 10 
Sample Input 2:
2
3 3 
1 2 3 
4 5 6 
7 8 9
3 1
10
20
30
Sample Output 2:
1 2 3 6 9 8 7 4 5 
10 20 30
```

```cpp
/*
#include <iostream>
using namespace std;

#include "solution.h"

int main()
{
    int t;
    cin >> t;
    while (t--)
    {

        int row, col;
        cin >> row >> col;
        int **matrix = new int *[row];

        for (int i = 0; i < row; i++)
        {
            matrix[i] = new int[col];
            for (int j = 0; j < col; j++)
            {
                cin >> matrix[i][j];
            }
        }
        spiralPrint(matrix, row, col);

        for (int i = 0; i < row; ++i)
        {
            delete[] matrix[i];
        }
        delete[] matrix;

        cout << endl;
    }
}
*/

/*-------------------------------CODE------------------------*/
void spiralPrint(int **input, int nRows, int mCols) { 
    int i, rowEnd = nRows-1, rowStart = 0, colEnd = mCols-1, colStart = 0; 
    int numElements = nRows * mCols, count = 0; 
    
    while (count < numElements) { 
        
        // ----->
        for (i = colStart; count < numElements && i <=colEnd; ++i) { 
            cout << input[rowStart][i] << " "; count++; 
        } 
        rowStart++; 
        
        // |
        // down
        for (i = rowStart; count < numElements && i <=rowEnd; ++i) { 
            cout << input[i][colEnd] << " "; count++; 
        } 
        colEnd--; 
        
        // <-----
        for (i = colEnd; count < numElements && i >= colStart; --i) { 
            cout << input[rowEnd][i] << " "; count++; 
        } 
        rowEnd--; 
        
        // up
        // |
        for (i = rowEnd; count < numElements && i >= rowStart; --i) { 
            cout << input[i][colStart] << " "; 
            count++; 
        } 
        colStart++; 
    } 
}
```

### Check Permutation

```
Check Permutation
 
For a given two strings, 'str1' and 'str2', check whether they are a permutation of each other or not.
Permutations of each other
Two strings are said to be a permutation of each other when either of the string's characters can be rearranged so that it becomes identical to the other one.

Example: 
str1= "sinrtg" 
str2 = "string"

The character of the first string(str1) can be rearranged to form str2 and hence we can say that the given strings are a permutation of each other.
Input Format:
The first line of input contains a string without any leading and trailing spaces, representing the first string 'str1'.

The second line of input contains a string without any leading and trailing spaces, representing the second string 'str2'.
Note:
All the characters in the input strings would be in lower case.
Output Format:
The only line of output prints either 'true' or 'false', denoting whether the two strings are a permutation of each other or not.

You are not required to print anything. It has already been taken care of. Just implement the function. 
Constraints:
0 <= N <= 10^6
Where N is the length of the input string.

Time Limit: 1 second
Sample Input 1:
abcde
baedc
Sample Output 1:
true
Sample Input 2:
abc
cbd
Sample Output 2:
false
```

```cpp
/*
#include <iostream>
#include <cstring>
using namespace std;

#include "solution.h"

int main() {
    int size = 1e6;
    char str1[size];
    char str2[size];
    cin >> str1 >> str2;
    cout << (isPermutation(str1, str2) ? "true" : "false");
}
*/

/*-------------------------------CODE------------------------*/
/*Time complexity: O(N + M) Space complexity: O(1) where N and M are the lengths of the two input strings */
bool isPermutation(char input1[], char input2[])
{
	int frequency[256];
	for (int i = 0; i < 256; ++i)
	{
		frequency[i] = 0;
	}
	for (int i = 0; input1[i] != '\0'; ++i)
	{
		++frequency[input1[i]];
	}
	for (int i = 0; input2[i] != '\0'; ++i)
	{
		--frequency[input2[i]];
	}
	for (int i = 0; i < 256; ++i)
	{
		if (frequency[i] != 0)
		{
			return false;
		}
	}
	return true;
}
```

### Remove Consecutive Duplicates

```
Remove Consecutive Duplicates
 
For a given string(str), remove all the consecutive duplicate characters.
Example:
Input String: "aaaa"
Expected Output: "a"

Input String: "aabbbcc"
Expected Output: "abc"
 Input Format:
The first and only line of input contains a string without any leading and trailing spaces. All the characters in the string would be in lower case.
Output Format:
The only line of output prints the updated string.
Note:
You are not required to print anything. It has already been taken care of.
Constraints:
0 <= N <= 10^6
Where N is the length of the input string.

Time Limit: 1 second
Sample Input 1:
aabccbaa
Sample Output 1:
abcba
Sample Input 2:
xxyyzxx
Sample Output 2:
xyzx
```

```cpp
/*
#include <iostream>
#include <cstring>
using namespace std;

#include "solution.h"

int main() {
    int size = 1e6;
    char str[size];
    cin >> str;
    removeConsecutiveDuplicates(str);
    cout << str;
}
*/

/*-------------------------------CODE------------------------*/
/*Time complexity: O(N) Space complexity: O(1) where N is the length of the input string */
void removeConsecutiveDuplicates(char input[]) {
    
    for(int i=1; input[i] != '\0'; ++i){
        if(input[i]==input[i-1]){
            input[i-1] = ' ';
        }
    }
    
    int index = 0;
    for(int i=0; input[i] != '\0'; ++i){
        if(input[i] != ' '){
            char temp = input[i];
            input[i] = input[index];
            input[index]= temp;
            index++;
        }
    }  
}
```

### Reverse Each Word

```
Reverse Each Word
 
Aadil has been provided with a sentence in the form of a string as a function parameter. The task is to implement a function so as to print the sentence such that each word in the sentence is reversed.
Example:
Input Sentence: "Hello, I am Aadil!"
The expected output will print, ",olleH I ma !lidaA".
Input Format:
The first and only line of input contains a string without any leading and trailing spaces. The input string represents the sentence given to Aadil.
Output Format:
The only line of output prints the sentence(string) such that each word in the sentence is reversed. 
Constraints:
0 <= N <= 10^6
Where N is the length of the input string.

Time Limit: 1 second
Sample Input 1:
Welcome to Coding Ninjas
Sample Output 1:
emocleW ot gnidoC sajniN
Sample Input 2:
Always indent your code
Sample Output 2:
syawlA tnedni ruoy edoc
```

```cpp
/*
#include <iostream>
#include <cstring>
using namespace std;

#include "solution.h"

int main() {
    int size = 1e6;
    char str[size];
    cin.getline(str, size);
    reverseEachWord(str);
    cout << str;
}
*/

/*-------------------------------CODE------------------------*/
//----------------WITHOUT USING ALGORITHM-------------------------
void reverseEachWord(char input[]) {
    int length = strlen(input);
    int start = 0, end=0;
    for(int i=0; i<= length; ++i){
        if(input[i] == '\0' || input[i]==' '){
            end=i-1;
            while(start<=end){
                // char temp = input[start];
                // input[start]=input[end];
                // input[end]=temp;
                swap(input[start],input[end]);
                start++;
                end--;
            }
            start = i + 1;
        }
        
    }
}

//----------------USING REVERSE ALGORITHM-------------------------
/*Time complexity: O(N) Space complexity: O(1) where N is the length of the input string */
#include <algorithm>
#include <cstring>

void reverseEachWord(char input[])
{
	int previous = -1;
	for (int i = 0; i <= strlen(input); i++)
	{
		if (input[i] == ' ' || input[i] == '\0')
		{
			reverse(input + previous + 1, input + i);
			previous = i;
		}
	}
}
```

### Remove character

```
Remove character
 
For a given a string(str) and a character X, write a function to remove all the occurrences of X from the given string.
The input string will remain unchanged if the given character(X) doesn't exist in the input string.
Input Format:
The first line of input contains a string without any leading and trailing spaces.

The second line of input contains a character(X) without any leading and trailing spaces.
Output Format:
The only line of output prints the updated string. 
Note:
You are not required to print anything explicitly. It has already been taken care of.
Constraints:
0 <= N <= 10^6
Where N is the length of the input string.

Time Limit: 1 second
Sample Input 1:
aabccbaa
a
Sample Output 1:
bccb
Sample Input 2:
xxyyzxx
y
Sample Output 2:
xxzxx
```

```cpp
/*
#include <iostream>
#include <cstring>
using namespace std;

#include "solution.h"

int main() {
    int size = 1e6;
    char str[size];
    cin.getline(str, size);
    char c;
    cin >> c;
    removeAllOccurrencesOfChar(str, c);
    cout << str;
}
*/

/*-------------------------------CODE------------------------*/

//-------------------MINE-------------------------
void removeAllOccurrencesOfChar(char input[], char c) {
    
    //FIRST APPROACH WITH EQUAL TO NULL VALUE
    int j=0, n = strlen(input);
    for(int i=0; i<=n; ++i){
        if(input[i]!=c){
        	input[j++]= input[i];
        }
    }
    
//     //SECOND APPROCAH WITH NULL VALUE PRINT
    int j=0, n = strlen(input);
    for(int i=0; i<n; ++i){
        if(input[i]!=c){
        	input[j++]= input[i];
        } 
    }
    input[j] = '\0';
}

//--------------CN------------------
/*Time complexity: O(N) Space complexity: O(1) where N is the length of the input string */
void removeAllOccurrencesOfChar(char input[], char c)
{
	int trim = 0;
	int i = 0;
	int len = strlen(input);
	while (i < len)
	{
		if (input[i] != c)
		{
			swap(input[i], input[trim]);
			i++;
			trim++;
		}
		else
		{
			input[i] = '\0';
			i++;
		}
	}
}
```

### Highest Occuring Character

```
Highest Occuring Character
 
For a given a string(str), find and return the highest occurring character.
Example:
Input String: "abcdeapapqarr"
Expected Output: 'a'
Since 'a' has appeared four times in the string which happens to be the highest frequency character, the answer would be 'a'.
If there are two characters in the input string with the same frequency, return the character which comes first.
Consider:
Assume all the characters in the given string to be in lowercase always.
Input Format:
The first and only line of input contains a string without any leading and trailing spaces.
Output Format:
The only line of output prints the updated string. 
Note:
You are not required to print anything explicitly. It has already been taken care of.
Constraints:
0 <= N <= 10^6
Where N is the length of the input string.

Time Limit: 1 second
Sample Input 1:
abdefgbabfba
Sample Output 1:
b
Sample Input 2:
xy
Sample Output 2:
x
```

```cpp
/*
#include <iostream>
#include <cstring>
using namespace std;

#include "solution.h"

int main() {
    int size = 1e6;
    char str[size];
    cin >> str;
    cout << highestOccurringChar(str);
}
*/

/*-------------------------------CODE------------------------*/
//------------------------MINE---------------------------------------
#include <cstring>
char highestOccurringChar(char input[]) {

    int length = strlen(input);
    int freq[256] = {0};
    
    for(int i=0; i<length; ++i){
        freq[input[i]]++; 
    }
    
    int max = freq[input[0]];
    char ans = input[0];
    
    for(int i=1; i<length; ++i){
        if(freq[input[i]]>max){
            max = freq[input[i]];
            ans=input[i];
        }
    }
    
    return ans;
}

//-------------------CN---------------------------
/*Time complexity: O(N) Space complexity: O(1) where N is the length of the input string */
char highestOccurringChar(char input[])
{
	int arr[26] = { 0 };
	int maxFreq = 0;
	for (int i = 0; input[i] != '\0'; i++)
	{
		arr[int(input[i]) - 'a'] += 1;
		maxFreq = max(maxFreq, arr[int(input[i]) - 'a']);
	}
	char ans;
	for (int i = 0; input[i] != '\0'; i++)
	{
		if (arr[int(input[i]) - 'a'] == maxFreq)
		{
			ans = input[i];
			break;
		}
	}
	return ans;
}
```


### Compress the String

```
Compress the String
 
Write a program to do basic string compression. For a character which is consecutively repeated more than once, replace consecutive duplicate occurrences with the count of repetitions.
Example:
If a string has 'x' repeated 5 times, replace this "xxxxx" with "x5".

The string is compressed only when the repeated character count is more than 1.
Note:
Consecutive count of every character in the input string is less than or equal to 9.
Input Format:
The first and only line of input contains a string without any leading and trailing spaces.
Output Format:
The output contains the string after compression printed in single line.
Note:
You are not required to print anything. It has already been taken care of. Just implement the given function.
Constraints:
0 <= N <= 10^6

Where 'N' is the length of the input string.

Time Limit: 1 sec
Sample Input 1:
aaabbccdsa
Sample Output 1:
a3b2c2dsa
Explanation for Sample Output 1:
In the given string 'a' is repeated 3 times, 'b' is repeated 2 times, 'c' is repeated 2 times and 'd', 's' and 'a' and occuring 1 time hence no compression for last 3 characters.
Sample Input 2:
aaabbcddeeeee
Sample Output 2:
a3b2cd2e5
Explanation for Sample Output 2:
In the given string 'a' is repeated 3 times, 'b' is repeated 2 times, 'c' is occuring single time, 'd' is repeating 2 times and 'e' is repeating 5times.
```

```cpp
/*
#include <iostream>
#include <cstring>
#include<string>
using namespace std;

#include "solution.h"

int main() {
    int size = 1e6;
    string str;
    cin >> str;
    str = getCompressedString(str);
    cout << str << endl;
}
*/

/*-------------------------------CODE------------------------*/
string getCompressedString(string &input) {
    
    int length = input.size();
    string output = "";
    
    for(int i=0; i<length; i++){
        int start = input[i];
        output += start;
        int ct=1;

        for(int j=i+1; j<length; ++j){
            if(input[j]==start){
                ct++;
                i++;
            }else{
                break;
            }
        }

        if(ct>1){
            output += to_string(ct);
        }
    }
    return output;
}
```

```

Lecture 10: Character Arrays and 2D Arrays END HERE

```

```

Lecture 10.5 : Test 2 START HERE

```

# ##Lecture 10.5 : Test 2

---

//============>>>>>>>>>> Lecture 10.5 : Test 2 Notes
PDF


---

###  Print 2D Array

```
Print 2D Array
 
Given a 2D integer array with n rows and m columns. Print the 0th row from input n times, 1st row n-1 times…..(n-1)th row will be printed 1 time.
Input format :
Line 1 : No of rows (n) and no of columns (m) (separated by single space)
Line 2 : Row 1 elements (separated by space)
Line 3 : Row 2 elements (separated by space)
Line 4 : and so on
Sample Input 1:
3 3
1 2 3
4 5 6
7 8 9
Sample Output 1 :
1 2 3
1 2 3
1 2 3
4 5 6
4 5 6
7 8 9
```

```cpp
/*
#include <iostream>
#include "solution.h"
using namespace std;

int main() {
    int row, col;
    cin >> row >> col;

    int **input = new int*[row];
    for(int i = 0; i < row; i++) {
	    input[i] = new int[col];
	    for(int j = 0; j < col; j++) {
	        cin >> input[i][j];
	    }
    }
    print2DArray(input, row, col);
}

*/

/*-------------------------------CODE------------------------*/
#include <iostream>
using namespace std;
void print2DArray(int **input, int row, int col)
{
	int k = row;
	for (int i = 0; i < row; i++)
	{
		for (int l = k - 1; l >= 0; l--)
		{
			for (int j = 0; j < col; j++)
			{
				cout << input[i][j] << " ";
			}
			cout << "\n";
		}
		k--;
	}
}
```

###  Minimum Length Word

```
Minimum Length Word
 
Given a string S (that can contain multiple words), you need to find the word which has minimum length.
Note : If multiple words are of same length, then answer will be first minimum length word in the string.
Words are seperated by single space only.
Input Format :
String S
Output Format :
Minimum length word
Constraints :
1 <= Length of String S <= 10^5
Sample Input 1 :
this is test string
Sample Output 1 :
is
Sample Input 2 :
abc de ghihjk a uvw h j
Sample Output 2 :
a
```

```cpp
/*
#include<iostream>
#include "solution.h"
using namespace std;


int main(){
  char ch[10000], output[10000];
  cin.getline(ch, 10000);
  minLengthWord(ch, output);
  cout << output << endl;
}

*/

/*-------------------------------CODE------------------------*/
/* input - Input String
*  output - Save the result in the output array (passed as argument). You don’t have to 
*  print or return the result
*/
#include <cstring>
void minLengthWord(char input[], char output[]){
		
  	
    int len = strlen(input);
    int start=0, end=0, min_len=len,  min_start_index = 0;
    while(end<=len){
        if(end<len && input[end] !=' '){
            end++;
        }else{
            int current_len = end-start;
            if(current_len<min_len){
                min_len= current_len;
                min_start_index = start;
            }
            
            end++;
            start=end;
        }
    }
    
    for(int i=0; i<min_len; ++i){
        output[i]= input[min_start_index++];
    }

}
```

###  Leaders in array

```
Leaders in array
 
Given an integer array A of size n. Find and print all the leaders present in the input array. An array element A[i] is called Leader, if all the elements following it (i.e. present at its right) are less than or equal to A[i].
Print all the leader elements separated by space and in the same order they are present in the input array.
Input Format :
Line 1 : Integer n, size of array
Line 2 : Array A elements (separated by space)
Output Format :
 leaders of array (separated by space)
Constraints :
1 <= n <= 10^6
Sample Input 1 :
6
3 12 34 2 0 -1
Sample Output 1 :
34 2 0 -1
Sample Input 2 :
5
13 17 5 4 6
Sample Output 2 :
17 6
```

```cpp
/*
#include<iostream>
#include<climits>
using namespace std;
#include"solution.h"
int main()
{
    int len;
    cin>>len;
	int *arr = new int[len + 1];
	
	for(int i=0;i<len;i++)
	{
		cin>>arr[i];
	}
	Leaders(arr,len);
}

*/

/*-------------------------------CODE------------------------*/
// Time Complexity of this code is O(n)
void Leaders(int *arr, int len)
{
	int j = 0;
	int *save = new int[len];
	int largest = INT_MIN;	//largest contains the maximum value of leading array. 
	for (int i = len - 1; i >= 0; i--)
	{
		if (arr[i] >= largest)	// if element at current index is greater than largest then put it in array and make ot largest; 
		{ 
			save[j] = arr[i];
			j++;
			largest = arr[i];
		}
	}
	for (int i = j - 1; i >= 0; i--)	// Print the array in reverse order... 
	{
		cout << save[i] << " ";
	}
}
```

```

Lecture 10.5 : Test 2 END HERE

```