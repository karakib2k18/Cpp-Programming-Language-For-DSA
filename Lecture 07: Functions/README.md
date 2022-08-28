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