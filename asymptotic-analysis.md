# Asymptotic Notation

Asymptotic notation is a way to describe the running time or space complexity of an algorithm based on the input size. It is commonly used in complexity analysis to describe how an algorithm performs as the size of the input grows. Following three of these notations are most commonly used.


## 1. Big-O Notation ($O$)

   - Provides an upper bound on the growth rate of an algorithm's running time or space usage

   - Represents the worst-case scenario

     - The maximum amount of time or space an algorithm may need to solve a problem

   - If an algorithm's running time is $O(n)$, the running time increases linearly with the input size $n$, or less


## 2. Omega Notation ($\Omega$)

   - Provides a lower bound on the growth rate of an algorithm's running time or space usage

   - Represents the best-case scenario

     - The minimum amount of time or space an algorithm may need to solve a problem

   - If an algorithm's running time is $\Omega(n)$, the running time increase linearly with the input size $n$, or more


## 3. Theta Notation ($\Theta$)

   - Provides both upper and lower bound on the growth rate of an algorithm's running time or space usage

   - Represents the average-case scenario

     - The amount of time or space an algorithm typically needs to solve a problem

   - If an algorithm's running time is $\Theta(n)$, the running time increase linearly with the input size $n$


Asymptotic notation does not provide an exact running time or space usage for an algorithm, but rather a description of how the algorithm scales with respect to input size. It is a useful tool for comparing the efficiency of different algorithms and for predicting how they will perform on large input sizes.


## What is Experimental Analysis?

- A way of comparing algorithms by running those programs for different inputs and find which one takes less time

- In this way, the algorithm with better performance may vary depending on the input

  - The running times of inputs that may be important could be left out and not be included in the experiment


## Advantages and Disadvantages of Asymptotic Analysis

### Advantage

- Provides a high-level understanding of how an algorithm performs with respect to input size

- Useful in comparing the efficiency of different algorithms and selecting the best one for a specific problem

- Helps in predicting how an algorithm will perform on larger input sizes

  - Essential for real-world applications

- Relatively easily performable and requires only basic mathematical skills

### Disadvantage

- Does not provide an accurate running time or space usage of an algorithm

- Assumes the input size as the only factor that affects an algorithm's performance, which is not always the case in practice

- Algorithms with the same asymptotic complexity may have different actual running times or space usage

- Determining the best asymptotic complexity is not always straightforward

  - Trade-offs between time and space complexity may exist


## Sources

GeeksforGeeks (2023, May 4). *Asymptotic Notation and Analysis (Based on input size) in Complexity Analysis of Algorithms*. [Link](https://www.geeksforgeeks.org/asymptotic-notation-and-analysis-based-on-input-size-of-algorithms/)
