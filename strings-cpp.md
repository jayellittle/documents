# Strings

### Define string

```cpp
string s = "Hello";
```

### Length of string

```cpp
cout << s.size() << endl;
```

```
5
```

### Element $i$ of string

```cpp
cout << s.at(1) << endl;
```

```
e
```

### Replace element of string

```cpp
s.at(0) = 'M';
cout << s << endl;
```

```
Mello
```

### Comparing strings

|Operator|Definition|
|----|--|
|`==`|Both strings are identical|
|`!=`|Both strings are different|
|`<` `<=` `>` `>=`|Compare both strings in dictionary order|

### Connecting string with string

- Operator `+`

```cpp
cout << s + ", world!" << endl;
```

```
Hello, world!
```

- Operator `+=`

```cpp
s += ", GitLab!";
cout << hello << endl;
```

```
Hello, GitLab!
```

### Connecting string with char

```cpp
char c = '!';
cout << s + c << endl;
```

```
Hello!
```

### Inserting string input in char value

```cpp
char c1, c2;
cin >> c1 >> c2;

cout << c1 << endl;
cout << c2 << endl;
```

```
OK
```

```
O
K
```

### Escape Sequence

```cpp
cout << "Hello\nWorld!";
```

```
Hello
World!
```

|Escape Sequence|Explanation|
|--|--|
|`\n`|Line alignment|
|`\"`|Double quotation mark|
|`\'`|Quotation mark|
|`\\`|Backslash|
|`\t`|Tab (Horizontal)|
|`\r`|Return|

### Inserting string input by lines

```cpp
string s1, s2;
getline(cin, s1);
getline(cin, s2);

cout << s1 << endl;
cout << s2 << endl;
```

```
Hello world!
My name is GitLab
```

```
Hello world!
My name is GitLab
```

## Convert string to int

### stoi() Function

```cpp
int stoi(string str, size_t position = 0, int base = 10);
```

#### Parameters

- str : String to be converted (compulsory)

- position : Starting position (optional, with value = 0)

- base : base of the number system (optional, with value = 10)

<details>
  <summary>Example</summary>
  
  ```cpp
  #include <iostream>
  #include <string>

  int main()
  {
    string s1 = "12";
    string s2 = "3.14";

    cout << stoi(s1) << endl;
    cout << stoi(s2) << endl;
  }
  ```

  ```
  12
  3
  ```
</details>

## Sources
- AtCoder. *C++入門 AtCoder Programming Guide for beginners*. [Link](https://atcoder.jp/contests/apg4b/tasks/APG4b_m)
- Geeksforgeeks. *Convert String to int in C++*. [Link](https://www.geeksforgeeks.org/convert-string-to-int-in-cpp/)
