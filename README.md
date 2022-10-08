# Fibonacci sequence report
![alt text](https://tumamocsketchbook.com/wp-content/uploads/2021/05/Screen-Shot-2021-05-26-at-6.04.09-PM-1024x661.png)

**The fibonacci sequence** is the series of numbers:

0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ...

The next number is found by adding up the two numbers before it

learn more through [ The Fibonacci Sequence: Nature's Code](https://youtu.be/wTlw7fNcO-0)
## Solutions for fibonacci sequence problem.

1.  **Recursion** 
2. **Vector**
3. **Changing space**

### First solution: *Recursion*
    Using the formula Fib[n]=Fib[n-1]+Fib[n-2]

**The code**

`#include <iostream> ` 

`using namespace std; ` 

`int Fib(int a){ ` 

` if (a==0 || a== 1){`  

`  return a ; ` 

` } ` 

` return Fib(a-1) + Fib(a-2) ; ` 

`}  `

`int main() {`  

` int n; ` 

`  cin>> n;`  

`cout<<Fib(n);`  

` return 0;`  

`  }`

### Second solution: *Vector*

 **The code**
 
 `#include <iostream> ` 

`#include <vector>  `

`using namespace std;  `

`int main() {  `

`vector<int> Fib {0,1};  `

`int n;  `

`cin>> n;  `

`for (int i = 2; i <=n ; i++) {  `

`      Fib[i]=Fib[i-1]+Fib[i-2];  `

`}  `

`cout<< Fib[n];`  

`return 0;`  

`}`

### Third solution: *Changing space*

**The code**

`#include<iostream>`

`using namespace std;`

`int Fib(int n){`

`int a = 0, b = 1, c, i;`

`if( n == 0)`

	`return a;`

`	for(i = 2; i <= n; i++)`

`	{`

`c = a + b;`

`	a = b;`

`b = c;`

`}`

`return b;`

`}`



`int main()`

`{`

`int n = 9;`

`cout << fib(n);`

`	return 0;`

`}`

### Summarizing the space and time complexity in the table.

| **Method** | **Space complexity** | Time complexity |
| ----------- | ----------- |  ----------- | 
| *Recursion*| Exponential|  O(1)| 
| *Vector*| ----|  O(1)| 
| *Changing space*| O(n)|  O(1)| 
