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