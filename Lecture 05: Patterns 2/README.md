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