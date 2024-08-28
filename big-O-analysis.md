# Big-O Analysis

The Big-O asymptotic notation gives the upper bound area, which can be described as following.

- $g$, $f$ are functions from $\mathbb{N}\rightarrow\mathbb{N}$ ($\mathbb{N}$ : The set of natural numbers)

- $f(n)=O(g(n))$, if there exists a positive integer $n_0$, and a positive constant $c$

  Constant $c$ is $f(n)\leq c\cdot g(n)$, for all $n\geq n_0$

- $O(g)$ is a set, but $f=O(g)$ does not mean $f\in O(g)$

<details>
<summary>Example</summary>

  　If $f(n)=n^4+100n^2+10n+50$, $g(n)=n^4$
  
</details>


## General stepwise procedure for Big-O runtime analysis

1. Figure out what the input is and what $n$ represents

   <details>
   <summary>Examples of input</summary>

   - Size of an array
     
   - Polynomial degree
  
   - Number of elements in a matrix
  
   - Number of bits in the binary representation of the input
  
   - Vertices and edges in a graph
   </details>  

2. Express the maximum number of operations the algorithm performs in terms of $n$

3. Eliminate all excluding the highest order terms

4. Remove all the constant factors


## Useful properties of Big-O notation analysis

- Constant Multiplication

  If $f(n)=c\cdot g(n)$, then $O(f(n))=O(g(n))$ ($c\neq 0$)
  
- Polynomial Function

  If $f(n)=a_0+a_1\cdot n+a_2\cdot n^2+\cdots+a_m\cdot n^m$, then $O(f(n))=O(n^m)$

- Summation Function

  If $f_1(n)+f_2(n)+\cdots+f_m(n)$ and $f_i(n)\leq f_{i+1}(n)$ for all $i=1,2,\cdots,m$,

  then $O(f(n))=O(\max(f_1(n),f_2(n),\cdots,f_m(n))$

- Logarithmic Function

  If $f(n)=\log_a{n}$ and $g(n)=\log_b{n}$, then $O(f(n))=O(g(n))$

  All log functions grow in the same manner in terms of Big-O

## Running Time Complexity

The algorithms can be classified as following from the best-to-worst performance.

- Constant algorithm : $O(1)$

  Gets a constant amount of runtime whatever the input size $n$ is

- Logarithmic algorithm : $O(\log{n})$

  Runtime grows logarithmically in proportion to $n$

- Linear algorithm : $O(n)$

  Runtime grows directly in proportion to $n$

- Superlinear(Linear Logarithmic) algorithm : $O(n\log{n})$

  Runtime grows in proportion to $n$

- Polynomial algorithm : $O(n^c)$

  Runtime grows quicker than previous, which is all based on $n$

- Exponential algorithm : $O(c^n)$

  Runtime grows even faster than polynomial algorithm based on $n$

- Factorial algorithm : $O(n!)$

  Runtime grows the fastest and becomes quicly unusable for even small values of $n$

($n$ : input size, $c$ : positive constant)

## Algorithmic Examples of Runtime Analysis

- $O(\log{n})$ → Binary Search

- $O(n)$ → Linear Search

- $O(n\log{n})$ → Heap Sort, Merge Sort

- $O(n^c)$ → Strassen's Matrix Multiplication, Bubble Sort, Selection Sort, Insertion Sort, Bucket Sort

- $O(c^n)$ → Tower of Hanoi

- $O(n!)$ → Determinant Expansion by Minors, Brute Force Search Algorithm for Traveling Salesman Problem

## Memory Footprint Analysis of Algorithms

For performance analysis of an algorithm, the amount of memory usage should be considered too.

This is referred to as the **memory footprint**, shortly known as *space complexity*.

## Space Complexity

The algorithms and its examples can be classified from the best-to-worst performance(space complexity) based on the worst-case scenarios as following.

- Ideal algorithm ( $O(1)$ ) : Linear Search, Binary Search, Bubble Sort, Selection Sort, Insertion Sort, Heap Sort, Shell Sort

- Logarithmic algorithm ( $O(\log{n})$ ) : Merge Sort

- Linear algorithm ( $O(n)$ ) : Quick Sort

- Sub-linear algorithm ( $O(n\log{n})$ ) : Radix Sort

## Sources

GeeksforGeeks. (2023, January 16). *Analysis of Algorithms | Big-O analysis*. [Link](https://www.geeksforgeeks.org/analysis-algorithms-big-o-analysis/)

Karumanchi Narasimha. (2011). *Data Structures And Algorithms Made Easy: Data Structures And Algorithmic Puzzles* (5th ed.). CareerMonk.
