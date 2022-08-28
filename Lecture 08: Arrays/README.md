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