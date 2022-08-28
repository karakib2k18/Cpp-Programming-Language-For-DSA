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