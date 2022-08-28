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