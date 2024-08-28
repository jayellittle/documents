# Data Structures of C++



## Arrays
- Size is specified when it is declared, and unchangeable afterward
- Multidimensional array
- Type `array` is stored in '`<array>`' library

### Declare an array
```cpp
int arr1[3] = {1, 2, 3};
array<int, 3> arr2 = {4, 5, 6};
```

### A multidimensional array
```cpp
int mat[3][3] = {
  {1, 2, 3},
  {4, 5, 6},
  {7, 8, 9}
};
```



## Vectors
- Stores sequence of elements which are accessible by index
- **Size is changeable**
- Stored in `<vector>` library

### Declare a vector
```cpp
vector<int> vec;
vec = {1, 1, 2, 3};
```

### Index an element in a vector
```cpp
cout << vec.at(2) << endl;

vec.at(2) = 8;
cout << vec.at(2) << endl;
cout << vec[2] << endl;
```
```
2
8
8
```

### Number of elements in a vector
```cpp
cout << vec.size() << endl;
```
```
4
```

### Reset a vector in certain option
```cpp
vector<int> vec1(4);
vector<int> vec2(4, 5);

int i;
for (i=0; i<vec1.size(); i++) {
  cout << vec1.at(i) << " ";
}
cout << endl;

for (i=0; i<vec2.size(); i++) {
  cout << vec2.at(i) << " ";
}
cout << endl;
```
```
0 0 0 0 
5 5 5 5 
```

### Add an element to the end of a vector
```cpp
cout << vec.size() << endl;

vec.push_back(9);
cout << vec.size() << endl;
cout << vec.at(vec.size() - 1) << endl;
```
```
4
5
9
```

### Remove the element at the end of a vector
```cpp
vec.pop_back();

cout << vec.size() << endl;
cout << vec.at(vec.size() - 1) << endl;
```
```
4
3
```

### Return whether a vector is empty or not
```cpp
cout << vec1.empty() << endl;

while (!vec1.empty()) vec1.pop_back();
cout << vec1.empty() << endl;
```
```
0
1
```

### Compare two vectors whether same or not
```cpp
vector<int> vec1 = {1, 2, 3};
vector<int> vec2 = {1, 2, 3};

if (vec1 == vec2) {
  cout << "OK" << endl;
}

// (vec1 == {1, 2, 3}) <- Compiler error
```


## Stacks and Queues
- Stores data in specific orders

|         |Stacks                                |Queues                                      |
|---------|--------------------------------------|--------------------------------------------|
|Order    |**LIFO**(Last In, First Out)          |**FIFO**(First In, First Out)               |
|Library  |`<stack>`                             |`<queue>`                                   |
|Index    |`.top()`                              |`.front()`, `.back()`                       |
|`.push()`|add an element at the top of the stack|remove the element at the top of the stack  |
|`.pop()` |add an element at the end of the queue|remove the element at the front of the queue|

<details>
<summary>Example</summary>

```cpp
#include <iostream>
#include <stack>
#include <queue>
using namespace std;

int main()
{
  stack<int> s1;
  s1.push(12);
  s1.push(24);
  s1.push(36);

  while(!s1.empty()) {
    cout << s1.top() << " ";
    s1.pop();
  }  // Output : 36 24 12
  cout << endl;

  queue<int> q1;
  q1.push(10);
  q1.push(20);
  q1.push(30);

  while(!q1.empty()) {
    cout << q1.front() << " ";
    q1.pop();
  }  // Output : 10 20 30
  cout << endl;

  return 0;
}
```

</details>


## Sets
- Contains collection of **unique** elements
- `<unordered_set>` or `<set>` library
  - `.insert()` : add an element to the set
  - `.erase()` : removes an element from the set
  - `.count()` : check whether an element exists in the set
  - `.size()` : return the size of the set

<details>
<summary>Example</summary>
 
```cpp
#include <iostream>
#include <unordered_set>
using namespace std;

int main()
{
  unordered_set<int> primes({2, 3, 5, 7});

  primes.insert(11);
  primes.insert(13);
  primes.insert(11);  // Ignored since it is a duplicate

  primes.erase(2);
  primes.erase(13);

  if (primes.count(2)) cout << "Contains 2" << endl; 
  else cout << "Does not contain 2" << endl;  // <- Output

  cout << "Size is " << primes.size() << endl;  // Output : Size is 4

  return 0;
}
```

</details>


## Hash Maps
- Collection of unique elements in the form of key-value pairs
- Each element is an object of type `pair`
  - `.first` : Value of the key
  - `.second` : Mapped value
- `<map>` or `<unordered_map>` library
  - `.insert()` : add an element to the map
  - `.erase()` : removes an element from the map
  - `.count()` : check whether an element exists in the map
  - `.size()` : return the size of the map
  - `[]` operator
    - If the specified key matches an element in the map → Access the mapped value associated with that key
    - If the specified key doesn't match any element in the map → Add a new element to the map with that key

<details>
<summary>Example</summary>

```cpp
#include <iostream>
#include <unordered_map>
using namespace std;

int main()
{
  unordered_map<string, int> country_codes;

  country_codes.insert({"Thailand", 65});
  country_codes.insert({"Peru", 51});
  country_codes["Japan"] = 81;  // Add a new element
  country_codes["Thailand"] = 66;  // Access an element

  country_codes.erase("Peru");

  if (country_codes.count("Belgium")) cout << "Yes" << endl;
  else cout << "No" << endl;  // Output : No

  cout << country_codes["Japan"] << endl;  // Output : 81

  cout << country_codes.size() << endl;  // Output : 2

  for (auto it: country_codes) {
    cout << it.first << " " << it.second << endl;
  }
  // Output : Japan 81
  //          Thailand 66

  return 0;
}
```

</details>


## Sources
- Codecademy. *C++'s Built-In Data Structures*. [Link](https://www.codecademy.com/learn/c-plus-plus-for-programmers/modules/cpp-built-in-data-structures/cheatsheet)
- AtCoder. *C++入門 AtCoder Programming Guide for beginners*. [Link](https://atcoder.jp/contests/apg4b/tasks/APG4b_n)
