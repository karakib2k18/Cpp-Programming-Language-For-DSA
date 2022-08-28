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